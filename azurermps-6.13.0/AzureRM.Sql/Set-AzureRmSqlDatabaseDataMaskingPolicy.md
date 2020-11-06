---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d59891980c11b90ee73275dbccb6a98b65c89613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493604"
---
# <span data-ttu-id="53439-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="53439-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="53439-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53439-102">SYNOPSIS</span></span>
<span data-ttu-id="53439-103">Adatmaszkolás beállítása egy adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="53439-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53439-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53439-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53439-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53439-105">DESCRIPTION</span></span>
<span data-ttu-id="53439-106">A **set-AzureRmSqlDatabaseDataMaskingPolicy** parancsmag az Azure SQL-adatbázisok adatmaszkolási házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="53439-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="53439-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="53439-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="53439-108">Beállíthatja, hogy az adatmaszkolási műveletek engedélyezve vagy Letiltva legyenek a *DataMaskingState* paraméterben.</span><span class="sxs-lookup"><span data-stu-id="53439-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="53439-109">Azt is megteheti, hogy az *PrivilegedLogins* paraméterrel megadhatja, hogy mely felhasználók láthatják a maszk nélküli adatot.</span><span class="sxs-lookup"><span data-stu-id="53439-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="53439-110">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, a program az adatbázis-azonosítók mellett az aktuális adatmaszkolási házirendet leíró objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="53439-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="53439-111">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="53439-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="53439-112">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="53439-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="53439-113">Példák</span><span class="sxs-lookup"><span data-stu-id="53439-113">EXAMPLES</span></span>

### <span data-ttu-id="53439-114">Példa 1: adatbázis adatmaszkolási házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="53439-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="53439-115">Ez a parancs beállítja a database01 nevű adatbázis adatmaszkolási házirendjét a server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="53439-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="53439-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53439-116">PARAMETERS</span></span>

### <span data-ttu-id="53439-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53439-117">-DatabaseName</span></span>
<span data-ttu-id="53439-118">Annak az adatbázisnak a nevét adja meg, amelyben a házirend van beállítva.</span><span class="sxs-lookup"><span data-stu-id="53439-118">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53439-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="53439-119">-DataMaskingState</span></span>
<span data-ttu-id="53439-120">Megadja, hogy az adatmaszkolási művelet engedélyezve vagy Letiltva van-e.</span><span class="sxs-lookup"><span data-stu-id="53439-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="53439-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="53439-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53439-122">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="53439-122">Enabled</span></span>
- <span data-ttu-id="53439-123">Letiltva: az alapértelmezett érték engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="53439-123">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53439-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53439-124">-DefaultProfile</span></span>
<span data-ttu-id="53439-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="53439-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53439-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53439-126">-PassThru</span></span>
<span data-ttu-id="53439-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="53439-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="53439-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="53439-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53439-129">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="53439-129">-PrivilegedLogins</span></span>
<span data-ttu-id="53439-130">Itt adhatja meg, hogy mely SQL-felhasználók kizárják a maszkolást.</span><span class="sxs-lookup"><span data-stu-id="53439-130">Specifies which SQL users are excluded from masking.</span></span>
<span data-ttu-id="53439-131">Ez a paraméter elavult, és a jövőbeli kiadásokból törlődik.</span><span class="sxs-lookup"><span data-stu-id="53439-131">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53439-132">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="53439-132">-PrivilegedUsers</span></span>
<span data-ttu-id="53439-133">A Kiemelt felhasználói azonosítók pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53439-133">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="53439-134">Ezek a felhasználók jogosultak a maszkolási adatmaszkolási szolgáltatás megtekintésére.</span><span class="sxs-lookup"><span data-stu-id="53439-134">These users are allowed to view the masking data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53439-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53439-135">-ResourceGroupName</span></span>
<span data-ttu-id="53439-136">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="53439-136">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53439-137">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="53439-137">-ServerName</span></span>
<span data-ttu-id="53439-138">Az adatbázist működtető kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53439-138">Specifies the name of the server hosting the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53439-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53439-139">-Confirm</span></span>
<span data-ttu-id="53439-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53439-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53439-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53439-141">-WhatIf</span></span>
<span data-ttu-id="53439-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53439-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53439-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53439-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53439-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53439-144">CommonParameters</span></span>
<span data-ttu-id="53439-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53439-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53439-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53439-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53439-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53439-147">INPUTS</span></span>

### <span data-ttu-id="53439-148">System. String</span><span class="sxs-lookup"><span data-stu-id="53439-148">System.String</span></span>

## <span data-ttu-id="53439-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53439-149">OUTPUTS</span></span>

### <span data-ttu-id="53439-150">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="53439-150">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="53439-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53439-151">NOTES</span></span>

## <span data-ttu-id="53439-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53439-152">RELATED LINKS</span></span>

[<span data-ttu-id="53439-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="53439-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="53439-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="53439-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="53439-155">Új – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="53439-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="53439-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="53439-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="53439-157">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="53439-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="53439-158">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="53439-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


