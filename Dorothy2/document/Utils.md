common\Utils.dms
================

���O���:
=========

Utils
-----
���[�e�B���e�B�֐��Q  
Utils�I�u�W�F�N�g

   * �����o�[:  

      * (�萔) UNDEFINED : {undefined}  

      * isDorothy2A : {boolean}  
         ���s����Dorothy2A�Ȃ��true  

      * isDorothy2set : {boolean}  
         ���s����Dorothy2set�Ȃ��true  

      * isDorothy2setList : {boolean}  
         ���s����OnListMenuClick��Dorothy2set(�uDorothy2�T�C�g�ݒ�v)�Ȃ��true  

      * isDOA : {boolean}  
         ���s����DOA�Ȃ��true  

      * isRentan : {boolean}  
         ���s����Dorothy2R�Ȃ��true  

      * queueFolder : {string}  
         folderdata.Post�̃R�����g�I�v�V��������擾�����L���[�t�H���_�̃p�X  

   * ���\�b�h:  

      * error(message, fileName, line, name) -> {String}  
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

      * showError(message, fileName, line, name) -> {String}  
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

      * isStr(v) -> {boolean}  
         ������Ƃ��Ĉ����邩���肵�܂� string String StringBuffer�Ȃ��true

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | v    | *  |      |
         

         * �߂�l:   

            * {boolean}

      * toStr(v) -> {string}  
         ������ɕϊ�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | v    | *  |      |
         

         * �߂�l:   

            * {string}

      * toNumber(v, def) -> {number|T}  
         ���l�ɕϊ� ���l�ɕϊ��ł��Ȃ����̂�NaN��Ԃ��܂��B

         * �p�����[�^:

         | ���O | �^ | ����   | ����                           |
         |------|----|--------|--------------------------------|
         | v    | *  |        |                                |
         | def  | T  | �ȗ��� | ���l�ɕϊ��ł��Ȃ��ꍇ�ɕԂ��l |
         

         * �߂�l:   

            * {number|T}

      * toInteger(v) -> {number}  
         �����l�ɕϊ�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | v    | *  |      |
         

         * �߂�l:   

            * {number}

      * objToPrimitive(v) -> {string|number|boolean|null|undefined}  
         �I�u�W�F�N�g���v���~�e�B�u�l�ɕϊ�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | v    | *  |      |
         

         * �߂�l:   

            * {string|number|boolean|null|undefined}

      * strToPrimitive(s) -> {string|number|boolean|null|undefined}  
         ��������v���~�e�B�u�l�ɕϊ�
         ��: "true" -> true

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | s    | *  |      |
         

         * �߂�l:   

            * {string|number|boolean|null|undefined}

      * extractName(s) -> {string}  
         �n���ꂽ�l����t�@�C���������o���܂�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | s    | *  |      |
         

         * �߂�l:   

            * {string} : �t�@�C����

      * extractExt(s) -> {string}  
         �n���ꂽ�l����g���q�����o���܂�

         * �p�����[�^:

         | ���O | �^ | ���� |
         |------|----|------|
         | s    | *  |      |
         

         * �߂�l:   

            * {string} : �t�@�C����

      * formatTemplate(s, map) -> {string}  
         �n���ꂽ�����񂩂� �u���ϐ�(%�`%) ��u�����Đ��`���܂�  
         map�̃v���p�e�B�Ɠ����̒u���ϐ������̒l�Œu�������܂� map�ɑ��݂��Ȃ����O�̒u���ϐ��͍폜����܂�

         * �p�����[�^:

         | ���O | �^     | ����   | ����                             |
         |------|--------|--------|----------------------------------|
         | s    | string |        |                                  |
         | map  | Object | �ȗ��� | �u�������Ɏg�p�����I�u�W�F�N�g |
         

         * �߂�l:   

            * {string} : ���`����������

      * call(fn, selfObj, var_args) -> {*}  
         .call()�̑�� �֐��̃��[�h��ύX�����ɌĂяo���܂��B �߂�l�œn�����֐��������Ō��Ƃ͕ʂ̊֐��Ƃ��Ĉ�����̂𗘗p���Ă��܂�

         * �p�����[�^:

         | ���O     | �^       | ����   | ����                                 |
         |----------|----------|--------|--------------------------------------|
         | fn       | function |        | �Ăяo���֐�                         |
         | selfObj  | *        |        | �֐�fn�̓�����this�Ƃ��Ďg�p�����l |
         | var_args | *        | �ϒ� | �֐�fn�ɓn��������                 |
         

         * �߂�l:   

            * {*} : �֐�fn�̕Ԃ�l

      * apply(fn, selfObj, argsArray) -> {*}  
         .apply()�̑�� �֐��̃��[�h��ύX�����ɌĂяo���܂�

         * �p�����[�^:

         | ���O      | �^       | ����     | ����                                           |
         |-----------|----------|----------|------------------------------------------------|
         | fn        | function |          | �Ăяo���֐�                                   |
         | selfObj   | *        |          | �֐�fn�̓�����this�Ƃ��Ďg�p�����I�u�W�F�N�g |
         | argsArray | Array    | null���e | �֐�fn�ɓn��������                           |
         

         * �߂�l:   

            * {*} : �֐�fn�̕Ԃ�l

      * getObject(name, obj, def) -> {*}  
         �w�肵�����S�C�����̃I�u�W�F�N�g���擾���܂� obj���w�肵���ꍇ��obj�̃v���p�e�B����擾���܂�

         * �p�����[�^:

         | ���O | �^     | ����   | ����                                                                                          |
         |------|--------|--------|-----------------------------------------------------------------------------------------------|
         | name | string |        | ���S�C���� ��: Global.Utils.UNDEFINED ��                                                      |
         | obj  | *      | �ȗ��� | ���̃I�u�W�F�N��ΏۂƂ��܂� �ȗ������ꍇ�O���[�o���X�R�[�v��Global�I�u�W�F�N�g��ΏۂƂ��܂� |
         | def  | *      | �ȗ��� | ������Ȃ������ꍇ�ɕԂ��l                                                                  |
         

         * �߂�l:   

            * {*}

      * keys(obj) -> {Array<string>}  
         �I�u�W�F�N�g�̑S�Ẵv���p�e�B����z��ŕԂ��܂��B

         * �p�����[�^:

         | ���O | �^ | ����         |
         |------|----|--------------|
         | obj  | *  | �I�u�W�F�N�g |
         

         * �߂�l:   

            * {Array<string>}

      * extend(var_args) -> {*}  
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

      * objCreate(ctorName, proto, prop) -> {Object}  
         �w�肵���v���g�^�C�v�ƃv���p�e�B�ŐV�����I�u�W�F�N�g�𐶐����܂�

         * �p�����[�^:

         | ���O     | �^     | ����   | ����                                                                                                                                       |
         |----------|--------|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
         | ctorName | string |        | �����Ŏg�p����R���X�g���N�^�֐��̖��O�B DMonkey�ł�prototype�͓����̊֐����m�ŋ��L����܂��B ���L����������ꍇ�͈�ӂ̖��O�ɂ��Ă������� |
         | proto    | Object | �ȗ��� | �V�����I�u�W�F�N�g�̃v���g�^�C�v�ƂȂ�I�u�W�F�N�g                                                                                         |
         | prop     | Object | �ȗ��� | ���̃I�u�W�F�N�g�̊e�v���p�e�B��V�����I�u�W�F�N�g�ɒǉ�����                                                                               |
         

         * �߂�l:   

            * {Object}

      * inherits(childCtor, parentCtor)  
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

      * mixin(dest, src)  
         dest�I�u�W�F�N�g��src�I�u�W�F�N�g�̑S�Ẵ����o�[���R�s�[���܂�

         * �p�����[�^:

         | ���O | �^     | ���� |
         |------|--------|------|
         | dest | Object |      |
         | src  | Object |      |
         

      * bind(fn, selfObj, var_args) -> {function}  
         this��������������ꂽ�V���Ȋ֐��𐶐����ĕԂ��܂�

         * �p�����[�^:

         | ���O     | �^       | ����   | ����                                                                                                  |
         |----------|----------|--------|-------------------------------------------------------------------------------------------------------|
         | fn       | function |        | �ΏۂƂ���֐�                                                                                        |
         | selfObj  | Object   |        | �֐�����this�Ƃ��Ďg�p�����l                                                                        |
         | var_args | *        | �ϒ� | �֐��ɓn���������B �������ꂽ�֐����Ăяo�����Ɏw�肳�ꂽ�����͂����̌�̈����Ƃ��Ďg�p����܂��B |
         

         * �߂�l:   

            * {function}

      * strToDateTime(str) -> {number}  
         ������\���������Irvine�Ŏg�p����Ă���TDateTime�̐��l�ɕϊ����܂�

         * �p�����[�^:

         | ���O | �^     | ����                                                  |
         |------|--------|-------------------------------------------------------|
         | str  | string | �uyyyy/mm/dd hh:nn:ss�v�܂��́uhh:nn:ss�v�`���̕����� |
         

         * �߂�l:   

            * {number} : TDateTime�̐��l

      * dateTimeToStr(n, formatStr) -> {string}  
         Irvine�Ŏg�p����Ă���TDateTime�̐��l�������\��������ɕϊ����܂�

         * �p�����[�^:

         | ���O      | �^     | ����   | ����                                     |
         |-----------|--------|--------|------------------------------------------|
         | n         | number |        | TDateTime�̐��l                          |
         | formatStr | string | �ȗ��� | Date�I�u�W�F�N�g�ɂ�镶����ϊ����̏��� |
         

         * �߂�l:   

            * {string} : ������\��������

      * setFolderData()  
         folderdata�����݂��Ȃ��ꍇ��folderdata���`���܂�

      * getScriptVersion(path) -> {string|number}  
         �w�肵���X�N���v�g�̃o�[�W�������擾���܂�  
         Irvine��Dorothy2�̃X�N���v�g�ɑΉ����Ă��܂�

         * �p�����[�^:

         | ���O | �^     | ����                 |
         |------|--------|----------------------|
         | path | string | �X�N���v�g�̃t���p�X |
         

         * �߂�l:   

            * {string|number} : �X�N���v�g�̃o�[�W���� ���l�ɕϊ��\�ȏꍇ�͐��l����ȊO�͕�����

      * getSavePath() -> {string}  
         ���s���ʂɓK�؂ȃA�C�e���̕ۑ��p�X���擾���܂�  
         ���΃p�X�������ꍇ�͐�΃p�X�ɂȂ�܂ŏ��ɏ�ʃL���[�t�H���_�̕ۑ��p�X�ƘA�������Ă����܂�

         * �߂�l:   

            * {string}

      * getQueueFolderPath() -> {string}  
         ���݂̃A�C�e����Irvine�̃L���[�t�H���_�̃p�X���擾���܂�

         * �߂�l:   

            * {string}

      * getUserPath() -> {string}  
         Dorothy.userPath���擾���܂� Dorothy.userPath���g���Ȃ�DOA�p

         * �߂�l:   

            * {string}

      * getUserIniPath() -> {string}  
         Dorothy.userIniPath���擾���܂� Dorothy.userIniPath���g���Ȃ�DOA�p

         * �߂�l:   

            * {string}

      * getVersionDorothy2A() -> {number}  
         Dorothy2A.dms�̃o�[�W�������擾���܂� Dorothy2R�̏ꍇ��Dorothy.rVersion�̒l��Ԃ��܂�

         * �߂�l:   

            * {number}

      * getVersionDorothy2set() -> {number}  
         Dorothy2set.dms�̃o�[�W�������擾���܂� Dorothy2R�̏ꍇ��Dorothy.rVersion�̒l��Ԃ��܂�

         * �߂�l:   

            * {number}

      * getVersionDOA() -> {number}  
         DOA.dms�̃o�[�W�������擾���܂� Dorothy2R�̏ꍇ��Dorothy.rVersion�̒l��Ԃ��܂�

         * �߂�l:   

            * {number}

      * setDOA_IT()  
         <pre>
         DOA�X�N���v�g�p
         DOA.status��DOA_IT�ɂ��Aitem�̃v���p�e�B�ɓK�؂�DOA�̊e�l��ݒ肵�܂�
          DOA.name����ł͂Ȃ��̂Ȃ�    item.filename = DOA.name
          DOA.comment����ł͂Ȃ��̂Ȃ� item.comment += DOA.comment
          DOA.size��123.4MB ���̌`���̕�����(/^([\d\.]+)([KMG])?(B|Byte)?$/i)�Ȃ��
           �o�C�g�l�ɕϊ����� item.filesize �ɐݒ肵�܂�
         </pre>

      * getCommentOption(key, def) -> {string|number|boolean|null|undefined|T}  
         folderdata.Post��item.comment�ɐݒ肳�ꂽ�I�v�V��������w�肳�ꂽ���O�̃I�v�V�������擾���܂�  
         �I�v�V�����̊e�l�͓K�؂ȃv���~�e�B�u�l�ɕϊ�����܂�

         * �p�����[�^:

         | ���O | �^     | ����   | ����                                             |
         |------|--------|--------|--------------------------------------------------|
         | key  | string |        | �I�v�V�����̖��O                                 |
         | def  | T      | �ȗ��� | �w�肳�ꂽ�I�v�V���������݂��Ȃ������ꍇ�ɕԂ��l |
         

         * �߂�l:   

            * {string|number|boolean|null|undefined|T}

      * getCommentOptions(def) -> {Object}  
         folderdata.Post��item.comment�ɐݒ肳�ꂽ�S�ẴI�v�V�������擾���܂�  
         �I�v�V�����̊e�l�͓K�؂ȃv���~�e�B�u�l�ɕϊ�����܂�  
         def���w�肵���ꍇ�͎擾�����I�v�V������def���}�[�W�����V�����I�u�W�F�N�g��Ԃ��܂�

         * �p�����[�^:

         | ���O | �^     | ����   | ����         |
         |------|--------|--------|--------------|
         | def  | Object | �ȗ��� | �f�t�H���g�l |
         

         * �߂�l:   

            * {Object}

      * redefineDorothy()  
         ���ʂ̍��ق��Ȃ�ׂ����Ȃ��Ȃ�l��Dorothy�̊֐������Ē�`���܂�  
         DOA��Dorothy2A��Dorothy2set���̊��ʂɑ��݂����肵�Ȃ������肷��v���p�e�B��֐�����  
         �Ȃ�ׂ��S�Ă̊��Ŏg�p�ł���悤�ɂ��܂�

�ύX����:
=========

* 2015/12/03  version 1.0  
   �V�K�쐬  
   DorothyEx.dms�̂قڑS�Ă̋@�\��������ɓ�������  
