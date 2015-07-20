# pyskyx
python module to help interfacing with SoftwareBisque's TheSkyX
  

## Usage
''' >>> import skyx
>>> sx = skyx.SkyXConnection("192.168.192.44")
>>> sx.find("Saturn")
True
>>> sx.find("Vulcan")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "skyx.py", line 74, in find
    raise SkyxObjectNotFoundError(target)
skyx.SkyxObjectNotFoundError: 'Vulcan'
>>> sx.sky6ObjectInformation("Saturn")
{'sk6ObjInfoProp_DEC_2000': '-17.777434376248852', 'sk6ObjInfoProp_AZM': '192.3302592258289', 'sk6ObjInfoProp_RA_RATE_ASPERSEC': '-0.0009208590737941336', 'sk6ObjInfoProp_ALT': '18.11230835059689', 'sk6ObjInfoProp_DEC_RATE_ASPERSEC': '0.000022557601141670602', 'sk6ObjInfoProp_RA_2000': '15.760512194513813'}
>>> '''


## Running tests

The tests are written for py.test. An optional --host argument can be supplied
to py.test to specify where TheSkyX is running. e.g.  
 py.test -v --host=192.168.192.44
