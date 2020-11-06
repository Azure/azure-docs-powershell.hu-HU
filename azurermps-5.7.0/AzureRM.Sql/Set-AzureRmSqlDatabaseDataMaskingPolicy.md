---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 26d056b5ad9cdff22f0419f90fad17c3147e0e14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494280"
---
# <span data-ttu-id="00707-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="00707-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="00707-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00707-102">SYNOPSIS</span></span>
<span data-ttu-id="00707-103">Adatmaszkolás beállítása egy adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="00707-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00707-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00707-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00707-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00707-105">DESCRIPTION</span></span>
<span data-ttu-id="00707-106">A **set-AzureRmSqlDatabaseDataMaskingPolicy** parancsmag az Azure SQL-adatbázisok adatmaszkolási házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="00707-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="00707-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="00707-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="00707-108">Beállíthatja, hogy az adatmaszkolási műveletek engedélyezve vagy Letiltva legyenek a *DataMaskingState* paraméterben.</span><span class="sxs-lookup"><span data-stu-id="00707-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="00707-109">Azt is megteheti, hogy az *PrivilegedLogins* paraméterrel megadhatja, hogy mely felhasználók láthatják a maszk nélküli adatot.</span><span class="sxs-lookup"><span data-stu-id="00707-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="00707-110">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, a program az adatbázis-azonosítók mellett az aktuális adatmaszkolási házirendet leíró objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="00707-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="00707-111">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="00707-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="00707-112">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="00707-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="00707-113">Példák</span><span class="sxs-lookup"><span data-stu-id="00707-113">EXAMPLES</span></span>

### <span data-ttu-id="00707-114">Példa 1: adatbázis adatmaszkolási házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="00707-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="00707-115">Ez a parancs beállítja a database01 nevű adatbázis adatmaszkolási házirendjét a server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="00707-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="00707-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00707-116">PARAMETERS</span></span>

### <span data-ttu-id="00707-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00707-117">-DatabaseName</span></span>
<span data-ttu-id="00707-118">Annak az adatbázisnak a nevét adja meg, amelyben a házirend van beállítva.</span><span class="sxs-lookup"><span data-stu-id="00707-118">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00707-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="00707-119">-DataMaskingState</span></span>
<span data-ttu-id="00707-120">Megadja, hogy az adatmaszkolási művelet engedélyezve vagy Letiltva van-e.</span><span class="sxs-lookup"><span data-stu-id="00707-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="00707-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="00707-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00707-122">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="00707-122">Enabled</span></span>
- <span data-ttu-id="00707-123">Tiltva</span><span class="sxs-lookup"><span data-stu-id="00707-123">Disabled</span></span>

<span data-ttu-id="00707-124">Az alapértelmezett érték engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="00707-124">The default value is Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00707-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00707-125">-DefaultProfile</span></span>
<span data-ttu-id="00707-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="00707-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00707-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00707-127">-PassThru</span></span>
<span data-ttu-id="00707-128">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="00707-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="00707-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="00707-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00707-130">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="00707-130">-PrivilegedLogins</span></span>
<span data-ttu-id="00707-131">Itt adhatja meg, hogy mely SQL-felhasználók kizárják a maszkolást.</span><span class="sxs-lookup"><span data-stu-id="00707-131">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="00707-132">Ez a paraméter elavult, és a jövőbeli kiadásokból törlődik.</span><span class="sxs-lookup"><span data-stu-id="00707-132">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00707-133">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="00707-133">-PrivilegedUsers</span></span>
<span data-ttu-id="00707-134">A Kiemelt felhasználói azonosítók pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="00707-134">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="00707-135">Ezek a felhasználók jogosultak a maszkolási adatmaszkolási szolgáltatás megtekintésére.</span><span class="sxs-lookup"><span data-stu-id="00707-135">These users are allowed to view the masking data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00707-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00707-136">-ResourceGroupName</span></span>
<span data-ttu-id="00707-137">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="00707-137">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00707-138">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="00707-138">-ServerName</span></span>
<span data-ttu-id="00707-139">Az adatbázist működtető kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00707-139">Specifies the name of the server hosting the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00707-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00707-140">-Confirm</span></span>
<span data-ttu-id="00707-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00707-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00707-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00707-142">-WhatIf</span></span>
<span data-ttu-id="00707-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00707-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00707-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00707-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00707-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00707-145">CommonParameters</span></span>
<span data-ttu-id="00707-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00707-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00707-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00707-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00707-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00707-148">INPUTS</span></span>

### <span data-ttu-id="00707-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="00707-149">None</span></span>
<span data-ttu-id="00707-150">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="00707-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00707-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00707-151">OUTPUTS</span></span>

### <span data-ttu-id="00707-152">Microsoft. Azure. Command. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="00707-152">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="00707-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00707-153">NOTES</span></span>

## <span data-ttu-id="00707-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00707-154">RELATED LINKS</span></span>

[<span data-ttu-id="00707-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="00707-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="00707-156">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="00707-156">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="00707-157">Új – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="00707-157">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="00707-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="00707-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="00707-159">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="00707-159">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="00707-160">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="00707-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


