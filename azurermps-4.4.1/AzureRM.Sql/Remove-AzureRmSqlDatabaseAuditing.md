---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 30161db97a108b4a5612eb9fbf0d3d749b64a11e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680763"
---
# <span data-ttu-id="f4bf4-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="f4bf4-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="f4bf4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="f4bf4-103">Eltávolítja az adatbázis naplózását.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4bf4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4bf4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4bf4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="f4bf4-106">A **Remove-AzureRmSqlDatabaseAuditing** parancsmag eltávolítja az Azure SQL-adatbázisok naplózását.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="f4bf4-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f4bf4-108">A parancsmag futtatása után az adatbázis naplózása nem történik meg.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="f4bf4-109">Ha a parancs sikeres, és a *PassThru* paramétert használta, a parancsmag egy olyan objektumot ad eredményül, amely leírja az aktuális naplózási házirendet az adatbázis-azonosítók mellett.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="f4bf4-110">Az adatbázis-azonosítók tartalmazzák, de nem korlátozódnak a **ResourceGroupName** , a **kiszolgálónévre** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>

<span data-ttu-id="f4bf4-111">Ha eltávolít egy Azure SQL-adatbázis naplózását, a fenyegetések észlelése is törlődik.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>

<span data-ttu-id="f4bf4-112">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f4bf4-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f4bf4-113">EXAMPLES</span></span>

### <span data-ttu-id="f4bf4-114">1. példa: az Azure SQL-adatbázisok naplózásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f4bf4-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f4bf4-115">Ez a parancs eltávolítja a Database01 nevű adatbázis naplózását.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="f4bf4-116">Az adatbázis az Server01-on található, amely a ResourceGroup01 nevű erőforráscsoport számára van társítva.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f4bf4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4bf4-117">PARAMETERS</span></span>

### <span data-ttu-id="f4bf4-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4bf4-118">-DatabaseName</span></span>
<span data-ttu-id="f4bf4-119">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f4bf4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4bf4-120">-PassThru</span></span>
<span data-ttu-id="f4bf4-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-121">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f4bf4-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4bf4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4bf4-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4bf4-124">Az adatbázist tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-124">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="f4bf4-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f4bf4-125">-ServerName</span></span>
<span data-ttu-id="f4bf4-126">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-126">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="f4bf4-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4bf4-127">-Confirm</span></span>
<span data-ttu-id="f4bf4-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4bf4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4bf4-129">-WhatIf</span></span>
<span data-ttu-id="f4bf4-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4bf4-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4bf4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4bf4-132">-DefaultProfile</span></span>
<span data-ttu-id="f4bf4-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4bf4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4bf4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4bf4-134">CommonParameters</span></span>
<span data-ttu-id="f4bf4-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4bf4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4bf4-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4bf4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4bf4-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4bf4-137">INPUTS</span></span>

### <span data-ttu-id="f4bf4-138">Microsoft. Azure. Command. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f4bf4-138">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="f4bf4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4bf4-139">OUTPUTS</span></span>

### <span data-ttu-id="f4bf4-140">Microsoft. Azure. Command. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f4bf4-140">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="f4bf4-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4bf4-141">NOTES</span></span>

## <span data-ttu-id="f4bf4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4bf4-142">RELATED LINKS</span></span>

[<span data-ttu-id="f4bf4-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f4bf4-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="f4bf4-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f4bf4-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="f4bf4-145">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f4bf4-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


