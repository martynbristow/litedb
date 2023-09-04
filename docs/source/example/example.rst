.. code-block:: python

   from litedb import DiskDatabase

   disk_db = DiskDatabase("~/.db")

    class DataRecord:

        def __init__(self, uid: int, payload: str):
            self.uid = day
            self.payload = str

        def __repr__(self) -> str:
            return str(self.__dict__)

    item_1 = DataRecord()
    item_2 = DataRecord()

    disk_db.insert(item_1)
    disk_db.insert(item_2)
    disk_db.commit()

    for item in disk_db.select(DataRecord):
        print(item)

    disk_db.select(DataRecord).clear()