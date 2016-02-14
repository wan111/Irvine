common\Utils.dms
================

���O���:
=========

Utils
-----
���[�e�B���e�B�֐��Q  
Utils�I�u�W�F�N�g

   * �����o�[:  

      * < static, constant > UNDEFINED : {undefined}  

      * < static > isDorothy2A : {boolean}  
         ���s����Dorothy2A�Ȃ��true  

      * < static > isDorothy2set : {boolean}  
         ���s����Dorothy2set�Ȃ��true  

      * < static > isDorothy2ListMenu : {boolean}  
         ���s����OnListMenuClick��Dorothy2set(�uDorothy2�T�C�g�ݒ�v)�Ȃ��true  

      * < static > isDOA : {boolean}  
         ���s����DOA�Ȃ��true  

      * < static > isRentan : {boolean}  
         ���s����Dorothy2R�Ȃ��true  

      * < static > queueFolder : {string}  
         folderdata.Post�̃R�����g�I�v�V��������擾�����L���[�t�H���_�̃p�X  

   * ���\�b�h:  

      * < static > error(message, fileName, line, name) �� {String}  
         �G���[���b�Z�[�W�𐮌`���ĕԂ��܂�

         * �p�����[�^:

         | ���O     | �^            | ����   | ����l                   | ����             |
         |----------|---------------|--------|--------------------------|------------------|
         | message  | string        |        |                          | �G���[���b�Z�[�W |
         | fileName | string        | �ȗ��� | Dorothy.matchFile+'.dms' | �t�@�C����       |
         | line     | string,number | �ȗ��� | ''                       | �G���[�����ӏ�   |
         | name     | string        | �ȗ��� | 'Error'                  | �G���[��         |
         

         * �߂�l:   

            * {String} : ���`�����������String�I�u�W�F�N�g �e�������v���p�e�B�ɒǉ�

      * < static > showError(message, fileName, line, name) �� {String}  
         �G���[���b�Z�[�W�𐮌`����alert�ŕ\�����܂�

         * �p�����[�^:

         | ���O     | �^            | ����   | ����l                   | ����             |
         |----------|---------------|--------|--------------------------|------------------|
         | message  | string        |        |                          | �G���[���b�Z�[�W |
         | fileName | string        | �ȗ��� | Dorothy.matchFile+'.dms' | �t�@�C����       |
         | line     | string,number | �ȗ��� | ''                       | �G���[�����ӏ�   |
         | name     | string        | �ȗ��� | 'Error'                  | �G���[��         |
         

         * �߂�l:   

            * {String} : ���`�����������String�I�u�W�F�N�g �e�������v���p�e�B�ɒǉ�

      * < static > isStr(v) �� {boolean}  
         ������Ƃ��Ĉ����邩���肵�܂� string String StringBuffer�Ȃ��true

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | v    | *  |      |
         

         * �߂�l:   

            * {boolean}

      * < static > toStr(v) �� {string}  
         ������ɕϊ�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | v    | *  |      |
         

         * �߂�l:   

            * {string}

      * < static > toNumber(v, def) �� {number|T}  
         ���l�ɕϊ� ���l�ɕϊ��ł��Ȃ����̂�NaN��Ԃ��܂��B

         * �p�����[�^:

         | ���O | �^ | ����   | ����                           |
         |------|----|--------|--------------------------------|
         | v    | *  |        |                                |
         | def  | T  | �ȗ��� | ���l�ɕϊ��ł��Ȃ��ꍇ�ɕԂ��l |
         

         * �߂�l:   

            * {number|T}

      * < static > toInteger(v) �� {number}  
         �����l�ɕϊ�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | v    | *  |      |
         

         * �߂�l:   

            * {number}

      * < static > objToPrimitive(v) �� {string|number|boolean|null|undefined}  
         �I�u�W�F�N�g���v���~�e�B�u�l�ɕϊ�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | v    | *  |      |
         

         * �߂�l:   

            * {string|number|boolean|null|undefined}

      * < static > strToPrimitive(s) �� {string|number|boolean|null|undefined}  
         ��������v���~�e�B�u�l�ɕϊ�
         ��: "true" -> true

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | s    | *  |      |
         

         * �߂�l:   

            * {string|number|boolean|null|undefined}

      * < static > extractPath(s) �� {string}  
         �n���ꂽ�l����p�X�����o���܂�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | s    | *  |      |
         

         * �߂�l:   

            * {string} : �p�X

      * < static > extractName(s) �� {string}  
         �n���ꂽ�l����t�@�C���������o���܂�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | s    | *  |      |
         

         * �߂�l:   

            * {string} : �t�@�C����

      * < static > extractExt(s) �� {string}  
         �n���ꂽ�l����g���q�����o���܂�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | s    | *  |      |
         

         * �߂�l:   

            * {string} : �g���q

      * < static > formatTemplate(s, map) �� {string}  
         �n���ꂽ�����񂩂� �u���ϐ�(%�`%) ��u�����Đ��`���܂�  
         map�̃v���p�e�B�Ɠ����̒u���ϐ������̒l�Œu�������܂� map�ɑ��݂��Ȃ����O�̒u���ϐ��͍폜����܂�

         * �p�����[�^:

         | ���O | �^     | ����   | ����                             |
         |------|--------|--------|----------------------------------|
         | s    | string |        |                                  |
         | map  | Object | �ȗ��� | �u�������Ɏg�p�����I�u�W�F�N�g |
         

         * �߂�l:   

            * {string} : ���`����������

      * < static > call(fn, selfObj, var_args) �� {*}  
         .call()�̑�� �֐��̃��[�h��ύX�����ɌĂяo���܂��B �߂�l�œn�����֐��������Ō��Ƃ͕ʂ̊֐��Ƃ��Ĉ�����̂𗘗p���Ă��܂�

         * �p�����[�^:

         | ���O     | �^       | ����   | ����                                 |
         |----------|----------|--------|--------------------------------------|
         | fn       | function |        | �Ăяo���֐�                         |
         | selfObj  | *        |        | �֐�fn�̓�����this�Ƃ��Ďg�p�����l |
         | var_args | *        | �ϒ� | �֐�fn�ɓn��������                 |
         

         * �߂�l:   

            * {*} : �֐�fn�̕Ԃ�l

      * < static > apply(fn, selfObj, argsArray) �� {*}  
         .apply()�̑�� �֐��̃��[�h��ύX�����ɌĂяo���܂�

         * �p�����[�^:

         | ���O      | �^       | ����     | ����                                           |
         |-----------|----------|----------|------------------------------------------------|
         | fn        | function |          | �Ăяo���֐�                                   |
         | selfObj   | *        |          | �֐�fn�̓�����this�Ƃ��Ďg�p�����I�u�W�F�N�g |
         | argsArray | Array    | null���e | �֐�fn�ɓn��������                           |
         

         * �߂�l:   

            * {*} : �֐�fn�̕Ԃ�l

      * < static > has(obj, key) �� {boolean}  
         obj��key�������Ă��邩

         * �p�����[�^:

         | ���O | �^     | ���� |
         |------|--------|------|
         | obj  | object |      |
         | key  | string |      |
         

         * �߂�l:   

            * {boolean}

      * < static > getObject(name, obj, def) �� {*}  
         �w�肵�����S�C�����̃I�u�W�F�N�g���擾���܂� obj���w�肵���ꍇ��obj�̃v���p�e�B����擾���܂�

         * �p�����[�^:

         | ���O | �^     | ����   | ����                                                                                          |
         |------|--------|--------|-----------------------------------------------------------------------------------------------|
         | name | string |        | ���S�C���� ��: Global.Utils.UNDEFINED ��                                                      |
         | obj  | *      | �ȗ��� | ���̃I�u�W�F�N��ΏۂƂ��܂� �ȗ������ꍇ�O���[�o���X�R�[�v��Global�I�u�W�F�N�g��ΏۂƂ��܂� |
         | def  | *      | �ȗ��� | ������Ȃ������ꍇ�ɕԂ��l                                                                  |
         

         * �߂�l:   

            * {*}

      * < static > keys(obj) �� {Array<string>}  
         �I�u�W�F�N�g�̑S�Ẵv���p�e�B����z��ŕԂ��܂��B

         * �p�����[�^:

         | ���O | �^ | ����         |
         |------|----|--------------|
         | obj  | *  | �I�u�W�F�N�g |
         

         * �߂�l:   

            * {Array<string>}

      * < static > objectKeys(obj) �� {Array<string>}  
         �I�u�W�F�N�g���g�̑S�Ẵv���p�e�B����z��ŕԂ��܂��B  
         Array��ArrayLike Object�̏ꍇ�͂��̗v�f�̓Y�����܂݂܂�  
         �g���݃I�u�W�F�N�g�̒�`�ς݂̃v���p�e�B��v���g�^�C�v�`�F�C���̃v���p�e�B�͏����܂��B

         * �p�����[�^:

         | ���O | �^ | ����         |
         |------|----|--------------|
         | obj  | *  | �I�u�W�F�N�g |
         

         * �߂�l:   

            * {Array<string>}

      * < static > extend(var_args) �� {*}  
         <pre>
         �w�肵���ŏ��̃I�u�W�F�N�g�ɕ����̃I�u�W�F�N�g���}�[�W���ĕԂ��܂��B
         �I�u�W�F�N�g�̎w�肪������̏ꍇ�͂��̎���this�ɑ΂��ă}�[�W���܂�
         �}�[�W���ŏz�Q�Ƃ��L�����ꍇ�̓}�[�W��ł����l�̏z�\�����Č����܂�
         �}�[�W���ɃI�u�W�F�N�g�ȊO��String,StringBuffer�I�u�W�F�N�g���w�肵���ꍇ�͋�I�u�W�F�N�g{}�Ƃ��Ĉ����܂�
         Utils.extend([deep,] [same,] [destination,] source1[, source2[, ...]])
          deep: �ȗ��� true�Ȃ�ΐ[���R�s�[(deep copy) �f�t�H���g��false
          same: �ȗ��� true�Ȃ�Γ����̃v���p�e�B�͓����^�̏ꍇ�̂ݏ㏑�� �f�t�H���g��false
          destination: �ȗ���  �}�[�W�� �g������I�u�W�F�N�g �ȗ������ꍇ��this
          source1,2...: �}�[�W�� �I�u�W�F�N�g
         </pre>

         * �p�����[�^:

         | ���O     | �^ | ����   | ���� |
         |----------|----|--------|------|
         | var_args | *  | �ϒ� |      |
         

         * �߂�l:   

            * {*} : �}�[�W�����I�u�W�F�N�g

         * �g�p��:  

            ```
            ��1: Utils.extend(destination, source); //destination��soucre�̓��e���R�s�[
            ��2: Utils.extend(true, destination, source, source2); //destination��soucre��sourc2�̓��e���f�B�[�v�R�s�[
            ��3: Utils.extend(source); //Utils��source�̓��e���R�s�[
            ��4: Obj.extend = Utils.extend;
                 Obj.extend(source); //Obj��source�̓��e���R�s�[
            ```  

      * < static > objCreate(ctorName, proto, prop) �� {Object}  
         �w�肵���v���g�^�C�v�ƃv���p�e�B�ŐV�����I�u�W�F�N�g�𐶐����܂�

         * �p�����[�^:

         | ���O     | �^     | ����   | ����                                                                                                                                              |
         |----------|--------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
         | ctorName | string |        | �����Ŏg�p����R���X�g���N�^�֐��̖��O�B<br>    DMonkey�ł�prototype�͓����̊֐����m�ŋ��L����܂��B ���L����������ꍇ�͈�ӂ̖��O�ɂ��Ă������� |
         | proto    | Object | �ȗ��� | �V�����I�u�W�F�N�g�̃v���g�^�C�v�ƂȂ�I�u�W�F�N�g                                                                                                |
         | prop     | Object | �ȗ��� | ���̃I�u�W�F�N�g�̊e�v���p�e�B��V�����I�u�W�F�N�g�ɒǉ�����                                                                                      |
         

         * �߂�l:   

            * {Object}

      * < static > inherits(childCtor, parentCtor)  
         <pre>
         ���̃R���X�g���N�^����v���g�^�C�v���p�����܂��B�N���X�̌p�����[���I�Ɏ��������܂��B
         �e��prototype�� constructor �v���p�e�B��ǉ����܂��B �e���g�̃R���X�g���N�^�֐��ł��B
         �q��prototype�� _super �v���p�e�B��ǉ����܂��B �e�̃R���X�g���N�^�֐��ł��B
         �q��prototype�� _base ���\�b�h��ǉ����܂��B �e���\�b�h�̌Ăяo���Ɏg�p���܂��B
         function _base(selfObj, methodName, var_args)
          selfObj: �Ăяo�����this�ƂȂ�l �ʏ�͎��g���w�肵�Ă�������
          methodName: �Ăяo���e�̃��\�b�h�̖��O
          var_args: �e���\�b�h�ɓn������
         </pre>

         * �p�����[�^:

         | ���O       | �^       | ����                             |
         |------------|----------|----------------------------------|
         | childCtor  | function | �q�N���X�ƂȂ�R���X�g���N�^�֐� |
         | parentCtor | function | �e�N���X�ƂȂ�R���X�g���N�^�֐� |
         

         * �g�p��:  

            ```
            function Parent(a){this.a = a;}
            function Child(a){
                //�e�̌Ăяo����
                //��1:
                    this._base(this, 'constructor', a);
                //��2:
                    Utils.call(Parent, this, a);
                //��3:
                    Utils.call(Child.prototype._super, this, a);
                //��4(DMonkey�ŗL�̎d�l):
                    var super_ = Child.prototype._super;
                    super_(a);
                //��5(DMonkey�ŗL�̎d�l)
                    Parent(a);
                //�ʖڂȗ�1:
                    this._super(a);
                //�ʖڂȗ�2:
                    Child.prototype._super(a);
            }
            Utils.inherits(Child, Parent);
            ```  

      * < static > mixin(dest, src)  
         dest�I�u�W�F�N�g��src�I�u�W�F�N�g�̑S�Ẵ����o�[���R�s�[���܂�

         * �p�����[�^:

         | ���O | �^     | ���� |
         |------|--------|------|
         | dest | Object |      |
         | src  | Object |      |
         

      * < static > bind(fn, selfObj, var_args) �� {function}  
         this��������������ꂽ�V���Ȋ֐��𐶐����ĕԂ��܂�

         * �p�����[�^:

         | ���O     | �^       | ����   | ����                                                                                                  |
         |----------|----------|--------|-------------------------------------------------------------------------------------------------------|
         | fn       | function |        | �ΏۂƂ���֐�                                                                                        |
         | selfObj  | Object   |        | �֐�����this�Ƃ��Ďg�p�����l                                                                        |
         | var_args | *        | �ϒ� | �֐��ɓn���������B �������ꂽ�֐����Ăяo�����Ɏw�肳�ꂽ�����͂����̌�̈����Ƃ��Ďg�p����܂��B |
         

         * �߂�l:   

            * {function}

      * < static > loadIni(def, path) �� {Object}  
         ini�t�@�C������ݒ�l��ǂݍ��݃I�u�W�F�N�g�ŕԂ��܂�  
         �e�ݒ�l�͓K�؂ȃv���~�e�B�u�l�ɕϊ�����܂�  
         path��ini�t�@�C���̃p�X����Ini�I�u�W�F�N�g��n���Ă�������  
         Ini�I�u�W�F�N�g��n�����ꍇ�͂�������ݒ�l��ǂݍ��݂܂�  
         def���w�肵���ꍇ�͎擾�����I�v�V������def���}�[�W�����V�����I�u�W�F�N�g��Ԃ��܂�

         * �p�����[�^:

         | ���O | �^         | ����   | ����l              | ����                                 |
         |------|------------|--------|---------------------|--------------------------------------|
         | def  | Object     | �ȗ��� |                     | �f�t�H���g�l                         |
         | path | string,Ini | �ȗ��� | Dorothy.userIniPath | ini�t�@�C���̃p�X����Ini�I�u�W�F�N�g |
         

         * �߂�l:   

            * {Object}

      * < static > saveIni(data, path)  
         ini�t�@�C���ɐݒ�l��ۑ����܂�  
         data�I�u�W�F�N�g�ɑ��݂��Ȃ��Z�N�V������L�[�͍폜����܂�  
         path��ini�t�@�C���̃p�X����Ini�I�u�W�F�N�g��n���Ă�������  
         Ini�I�u�W�F�N�g��n�����ꍇ�͂����ɐݒ�l��ۑ����܂��B Ini�I�u�W�F�N�g�̓��e�͍X�V����܂�

         * �p�����[�^:

         | ���O | �^         | ����   | ����l              | ����                                          |
         |------|------------|--------|---------------------|-----------------------------------------------|
         | data | Object     |        |                     | ini�t�@�C���ɕۑ�����ݒ�l�����I�u�W�F�N�g |
         | path | string,Ini | �ȗ��� | Dorothy.userIniPath | ini�t�@�C���̃p�X����Ini�I�u�W�F�N�g          |
         

      * < static > loadOption(def, path, var_args) �� {Object}  
         ini�t�@�C���܂���JSON�t�@�C������ݒ�l��ǂݍ��݂܂�

         * �p�����[�^:

         | ���O     | �^         | ����   | ����l              | ����                                                         |
         |----------|------------|--------|---------------------|--------------------------------------------------------------|
         | def      | Object     | �ȗ��� |                     | �f�t�H���g�l                                                 |
         | path     | string,Ini | �ȗ��� | Dorothy.userIniPath | ini�t�@�C���̃p�X����Ini�I�u�W�F�N�g�A����JSON�t�@�C���̃p�X |
         | var_args | *          | �ϒ� |                     | JSON�t�@�C���̏ꍇ��JSON.load�ɓn������                      |
         

         * �߂�l:   

            * {Object}

      * < static > saveOption(data, path, var_args)  
         ini�t�@�C���܂���JSON�t�@�C���ɐݒ�l��ۑ����܂�  
         path��JSON�t�@�C���̃p�X����ini�t�@�C���̃p�X����Ini�I�u�W�F�N�g��n���Ă�������  
         Ini�I�u�W�F�N�g��n�����ꍇ�͂����ɐݒ�l��ۑ����܂��B Ini�I�u�W�F�N�g�̓��e�͍X�V����܂�

         * �p�����[�^:

         | ���O     | �^         | ����   | ����l              | ����                                                       |
         |----------|------------|--------|---------------------|------------------------------------------------------------|
         | data     | Object     |        |                     | �t�@�C���ɕۑ�����ݒ�l�����I�u�W�F�N�g                 |
         | path     | string,Ini | �ȗ��� | Dorothy.userIniPath | JSON�t�@�C���̃p�X����ini�t�@�C���̃p�X����Ini�I�u�W�F�N�g |
         | var_args | *          | �ϒ� |                     | JSON�t�@�C���̏ꍇ��JSON.save�ɓn������                    |
         

      * < static > strToDateTime(str) �� {number}  
         ������\���������Irvine�Ŏg�p����Ă���TDateTime�̐��l�ɕϊ����܂�

         * �p�����[�^:

         | ���O | �^     | ����                                                  |
         |------|--------|-------------------------------------------------------|
         | str  | string | �uyyyy/mm/dd hh:nn:ss�v�܂��́uhh:nn:ss�v�`���̕����� |
         

         * �߂�l:   

            * {number} : TDateTime�̐��l

      * < static > dateTimeToStr(n, formatStr) �� {string}  
         Irvine�Ŏg�p����Ă���TDateTime�̐��l�������\��������ɕϊ����܂�

         * �p�����[�^:

         | ���O      | �^     | ����   | ����                                     |
         |-----------|--------|--------|------------------------------------------|
         | n         | number |        | TDateTime�̐��l                          |
         | formatStr | string | �ȗ��� | Date�I�u�W�F�N�g�ɂ�镶����ϊ����̏��� |
         

         * �߂�l:   

            * {string} : ������\��������

      * < static > setFolderData()  
         folderdata�����݂��Ȃ��ꍇ��folderdata���`���܂�

      * < static > getScriptVersion(path) �� {string|number}  
         �w�肵���X�N���v�g�̃o�[�W�������擾���܂�  
         Irvine��Dorothy2�̃X�N���v�g�ɑΉ����Ă��܂�

         * �p�����[�^:

         | ���O | �^     | ����                 |
         |------|--------|----------------------|
         | path | string | �X�N���v�g�̃t���p�X |
         

         * �߂�l:   

            * {string|number} : �X�N���v�g�̃o�[�W���� ���l�ɕϊ��\�ȏꍇ�͐��l����ȊO�͕�����

      * < static > getSavePath() �� {string}  
         ���s���ʂɓK�؂ȃA�C�e���̕ۑ���̃p�X���擾���܂�  
         ���΃p�X�������ꍇ�͐�΃p�X�ɂȂ�܂ŏ��ɏ�ʃL���[�t�H���_�̕ۑ��p�X�ƘA�������Ă����܂�

         * �߂�l:   

            * {string}

      * < static > expandPath(path, base) �� {string}  
         path�����s���ʂɓK�؂ȕۑ���̐�΃p�X�ɕϊ����܂�  
         ���ɐ�΃p�X�������ꍇ�͉������܂���  
         ������ 'C:\aaa\..\bbb\' �̂悤�Ȏw��̏ꍇ�� "C:\bbb\' �ɕϊ�����܂�  
         base���w�肵���ꍇ��base����p�X�Ƃ��Ďg�p���܂�  
         �P���ɘA�������Ă��邾���Ȃ̂Ŋ�p�X�Ƀt�@�C�������܂܂��Ȃ��ŉ�����

         * �p�����[�^:

         | ���O | �^     | ����   | ����l | ����         |
         |------|--------|--------|--------|--------------|
         | path | string | �ȗ��� | ''     | �ϊ�����p�X |
         | base | string | �ȗ��� | ''     | ��p�X     |
         

         * �߂�l:   

            * {string}

      * < static > getQueueFolderPath() �� {string}  
         ���݂̃A�C�e����Irvine�̃L���[�t�H���_�̃p�X���擾���܂�

         * �߂�l:   

            * {string}

      * < static > getUserPath() �� {string}  
         Dorothy.userPath���擾���܂� Dorothy.userPath���g���Ȃ�DOA�p

         * �߂�l:   

            * {string}

      * < static > getUserIniPath() �� {string}  
         Dorothy.userIniPath���擾���܂� Dorothy.userIniPath���g���Ȃ�DOA�p

         * �߂�l:   

            * {string}

      * < static > getVersionDorothy2A() �� {number}  
         Dorothy2A.dms�̃o�[�W�������擾���܂� Dorothy2R�̏ꍇ��Dorothy.rVersion�̒l��Ԃ��܂�

         * �߂�l:   

            * {number}

      * < static > getVersionDorothy2set() �� {number}  
         Dorothy2set.dms�̃o�[�W�������擾���܂� Dorothy2R�̏ꍇ��Dorothy.rVersion�̒l��Ԃ��܂�

         * �߂�l:   

            * {number}

      * < static > getVersionDorothy2ListMenu() �� {number}  
         Dorothy2ListMenu.dms�̃o�[�W�������擾���܂� Dorothy2R�̏ꍇ��Dorothy.rVersion�̒l��Ԃ��܂�

         * �߂�l:   

            * {number}

      * < static > getVersionDOA() �� {number}  
         DOA.dms�̃o�[�W�������擾���܂� Dorothy2R�̏ꍇ��Dorothy.rVersion�̒l��Ԃ��܂�

         * �߂�l:   

            * {number}

      * < static > setDOA_IT()  
         <pre>
         DOA�X�N���v�g�p
         DOA.status��DOA_IT�ɂ��Aitem�̃v���p�e�B�ɓK�؂�DOA�̊e�l��ݒ肵�܂�
          DOA.name����ł͂Ȃ��̂Ȃ�    item.filename = DOA.name
          DOA.comment����ł͂Ȃ��̂Ȃ� item.comment += DOA.comment
          DOA.size��123.4MB ���̌`���̕�����(/^([\d\.]+)([KMG])?(B|Byte)?$/i)�Ȃ��
           �o�C�g�l�ɕϊ����� item.filesize �ɐݒ肵�܂�
         </pre>

      * < static > setDOA(itemData)  
         DOA�ɂĕs�����Ă���e�ϐ���v���p�e�B��ݒ肵�܂� DOA�X�N���v�g��main�֐����Ŗ���Ăяo���Ă�������

         * �p�����[�^:

         | ���O     | �^         | ����                   |
         |----------|------------|------------------------|
         | itemData | IrvineItem | main�֐����ł�itemData |
         

      * < static > doaItemAdd(url, filename, filesize, comment)  
         DOA��ʂɃA�C�e����ǉ����܂�

         * �p�����[�^:

         | ���O     | �^            | ����   | ����l | ����                     |
         |----------|---------------|--------|--------|--------------------------|
         | url      | string        |        |        | �A�C�e����URL            |
         | filename | string        | �ȗ��� | ''     | �A�C�e���̃t�@�C����     |
         | filesize | string,number | �ȗ��� | ''     | �A�C�e���̃t�@�C���T�C�Y |
         | comment  | string        | �ȗ��� | ''     | �A�C�e���̃R�����g       |
         

      * < static > doaItemAdd_IT(itemData)  
         DOA��ʂɃA�C�e����ǉ����܂� �ǉ������A�C�e����DOA.status��DOA_IT�ɂȂ�܂�

         * �p�����[�^:

         | ���O     | �^                | ����                                                                     |
         |----------|-------------------|--------------------------------------------------------------------------|
         | itemData | object,IrvineItem | IrvineItem�I�u�W�F�N�g�܂��͂���Ɠ������O�̃v���p�e�B�����I�u�W�F�N�g |
         

      * < static > getCommentOption(key, def) �� {string|number|boolean|null|undefined|T}  
         folderdata.Post��item.comment�ɐݒ肳�ꂽ�I�v�V��������w�肳�ꂽ���O�̃I�v�V�������擾���܂�  
         �I�v�V�����̊e�l�͓K�؂ȃv���~�e�B�u�l�ɕϊ�����܂�

         * �p�����[�^:

         | ���O | �^     | ����   | ����                                             |
         |------|--------|--------|--------------------------------------------------|
         | key  | string |        | �I�v�V�����̖��O                                 |
         | def  | T      | �ȗ��� | �w�肳�ꂽ�I�v�V���������݂��Ȃ������ꍇ�ɕԂ��l |
         

         * �߂�l:   

            * {string|number|boolean|null|undefined|T}

      * < static > getCommentOptions(def) �� {Object}  
         folderdata.Post��item.comment�ɐݒ肳�ꂽ�S�ẴI�v�V�������擾���܂�  
         �I�v�V�����̊e�l�͓K�؂ȃv���~�e�B�u�l�ɕϊ�����܂�  
         def���w�肵���ꍇ�͎擾�����I�v�V������def���}�[�W�����V�����I�u�W�F�N�g��Ԃ��܂�

         * �p�����[�^:

         | ���O | �^     | ����   | ����         |
         |------|--------|--------|--------------|
         | def  | Object | �ȗ��� | �f�t�H���g�l |
         

         * �߂�l:   

            * {Object}

      * < static > setCommentOption(key, value)  
         item.comment��key=value;�`���̃I�v�V������ݒ肵�܂�  
         �����̃I�v�V���������ɐݒ肳��Ă���ꍇ�͎w�肳�ꂽ�l�ŏ㏑�����܂�

         * �p�����[�^:

         | ���O  | �^     | ����             |
         |-------|--------|------------------|
         | key   | string | �I�v�V�����̖��O |
         | value | *      | �I�v�V�����̒l   |
         

      * < static > redefineDorothy()  
         ���ʂ̍��ق��Ȃ�ׂ����Ȃ��Ȃ�l��Dorothy�̊֐������Ē�`���܂�  
         DOA��Dorothy2A��Dorothy2set���̊��ʂɑ��݂����肵�Ȃ������肷��v���p�e�B��֐�����  
         �Ȃ�ׂ��S�Ă̊��Ŏg�p�ł���悤�ɂ��܂�

      * < static > checkVersion()  
         Dorothy�̊e���s���ŌÂ��o�[�W�������g�p����Ă��Ȃ����`�F�b�N���܂�  
         �Â��o�[�W�������g�p����Ă����ꍇ�̓G���[���b�Z�[�W��\�����ăX�N���v�g���I�����܂�

�ύX����:
=========

* 2016/02/14  version 1.5
   .objectKeys(), .setCommentOption() ��ǉ�

* 2016/02/04  version 1.4
   .setDOA(), .doaItemAdd(), .doaItemAdd_IT() ��ǉ�
   .redefineDorothy()�ɂ�DOA�̏ꍇ��.setDOA()�����s����悤�ɂ���

* 2016/01/26  version 1.3
   .extractPath(), .has(), .saveOption() ��ǉ�

* 2016/01/18  version 1.2  
   isDorothy2setList��isDorothy2ListMenu�ɕύX�B
   .getVersionDorothy2ListMenu()��ǉ��B
   .redefineDorothy���X�V urlinfo headers folderdata�̒�`���ǉ��B
   .checkVersion()��ǉ� �o�[�W�����`�F�b�N���s���l�ɂ����B

* 2015/12/12  version 1.1  
   loadIni(), saveIni(), loadOption() exxpandPath() ���\�b�h��V�K�ǉ��B  
   call(), apply()�ɂăG���[������ǉ��B 

* 2015/12/03  version 1.0  
   �V�K�쐬  
   DorothyEx.dms�̂قڑS�Ă̋@�\��������ɓ�������  

