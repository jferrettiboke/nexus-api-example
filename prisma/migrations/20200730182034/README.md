# Migration `20200730182034`

This migration has been generated by Jesús Ferretti at 7/30/2020, 6:20:34 PM.
You can check out the [state of the schema](./schema.prisma) after the migration.

## Database Steps

```sql
CREATE TABLE "public"."Post" (
"body" text  NOT NULL ,"id" SERIAL,"published" boolean  NOT NULL ,"title" text  NOT NULL ,
    PRIMARY KEY ("id"))
```

## Changes

```diff
diff --git schema.prisma schema.prisma
migration ..20200730182034
--- datamodel.dml
+++ datamodel.dml
@@ -1,0 +1,11 @@
+datasource postgres {
+    provider = "postgresql"
+    url = "***"
+}
+
+model Post {
+    id        Int     @id @default(autoincrement())
+    title     String
+    body      String
+    published Boolean
+}
```


