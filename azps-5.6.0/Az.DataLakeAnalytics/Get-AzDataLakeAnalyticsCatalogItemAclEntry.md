---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 63e0f3622ea7ae83f805688e4634b30c38cb601d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925001"
---
# <span data-ttu-id="3c87f-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3c87f-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="3c87f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c87f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c87f-103">Egy katalógus vagy katalóguselem ACL-ében kap egy bejegyzést a Data Lake Analytics szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="3c87f-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="3c87f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c87f-104">SYNTAX</span></span>

### <span data-ttu-id="3c87f-105">GetCatalogAclEntry (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c87f-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c87f-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="3c87f-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c87f-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="3c87f-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c87f-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3c87f-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c87f-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="3c87f-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c87f-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="3c87f-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c87f-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c87f-111">DESCRIPTION</span></span>
<span data-ttu-id="3c87f-112">A **Get-AzDataLakeAnalyticsCatalogItemAclEntry** parancsmag a Data Lake Analytics szolgáltatásban található katalógus vagy katalóguselem hozzáférés-vezérlési listájában (ACL) szereplő bejegyzések listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="3c87f-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="3c87f-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c87f-113">EXAMPLES</span></span>

### <span data-ttu-id="3c87f-114">1. példa: Katalógus ACL-ének lekérte</span><span class="sxs-lookup"><span data-stu-id="3c87f-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="3c87f-115">Ez a parancs lekérte a megadott Data Lake Analytics-fiók katalógusának ACL-ét</span><span class="sxs-lookup"><span data-stu-id="3c87f-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3c87f-116">2. példa: A felhasználó tulajdonosának ACL-bejegyzésének be szereznie egy katalógusban</span><span class="sxs-lookup"><span data-stu-id="3c87f-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="3c87f-117">Ez a parancs ACL-bejegyzést kap a felhasználó tulajdonosától a megadott Data Lake Analytics-fiók katalógusában</span><span class="sxs-lookup"><span data-stu-id="3c87f-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3c87f-118">3. példa: A csoporttulajdonos ACL-bejegyzésének be szereznie egy katalógusban</span><span class="sxs-lookup"><span data-stu-id="3c87f-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="3c87f-119">Ez a parancs ACL-bejegyzést kap a csoport tulajdonosától a megadott Data Lake Analytics-fiók katalógusában</span><span class="sxs-lookup"><span data-stu-id="3c87f-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3c87f-120">4. példa: Adatbázis ACL-ének lekérte</span><span class="sxs-lookup"><span data-stu-id="3c87f-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="3c87f-121">Ez a parancs lekérte a megadott Data Lake Analytics-fiók adatbázisának ACL-ét</span><span class="sxs-lookup"><span data-stu-id="3c87f-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3c87f-122">5. példa: Adatbázis felhasználói tulajdonosának ACL-bejegyzésének be szereznie</span><span class="sxs-lookup"><span data-stu-id="3c87f-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="3c87f-123">Ez a parancs a megadott Data Lake Analytics-fiók adatbázisának felhasználótulajdonosi ACL-bejegyzését kapja meg</span><span class="sxs-lookup"><span data-stu-id="3c87f-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="3c87f-124">6. példa: Adatbázis csoporttulajdonosICL-bejegyzésének be szereznie</span><span class="sxs-lookup"><span data-stu-id="3c87f-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="3c87f-125">Ez a parancs a megadott Data Lake Analytics-fiók adatbázisának csoporttulajdonosi ACL-bejegyzését kapja meg</span><span class="sxs-lookup"><span data-stu-id="3c87f-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="3c87f-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c87f-126">PARAMETERS</span></span>

### <span data-ttu-id="3c87f-127">-Account</span><span class="sxs-lookup"><span data-stu-id="3c87f-127">-Account</span></span>
<span data-ttu-id="3c87f-128">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c87f-128">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c87f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c87f-129">-DefaultProfile</span></span>
<span data-ttu-id="3c87f-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c87f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c87f-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="3c87f-131">-GroupOwner</span></span>
<span data-ttu-id="3c87f-132">A katalógus ACL-bejegyzésének lekérte a csoporttulajdonosnak</span><span class="sxs-lookup"><span data-stu-id="3c87f-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c87f-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="3c87f-133">-ItemType</span></span>
<span data-ttu-id="3c87f-134">A katalógus vagy katalóguselem(ök) típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3c87f-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="3c87f-135">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="3c87f-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3c87f-136">Katalógus</span><span class="sxs-lookup"><span data-stu-id="3c87f-136">Catalog</span></span>
- <span data-ttu-id="3c87f-137">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="3c87f-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c87f-138">-Path</span><span class="sxs-lookup"><span data-stu-id="3c87f-138">-Path</span></span>
<span data-ttu-id="3c87f-139">Egy katalógus vagy katalóguselem Data Lake Analytics-útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c87f-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="3c87f-140">Az elérési út egyes részeit pont (.) választja el egymástól.</span><span class="sxs-lookup"><span data-stu-id="3c87f-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c87f-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="3c87f-141">-UserOwner</span></span>
<span data-ttu-id="3c87f-142">A felhasználói tulajdonos katalógusának ACL-bejegyzését is lekérte.</span><span class="sxs-lookup"><span data-stu-id="3c87f-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c87f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c87f-143">CommonParameters</span></span>
<span data-ttu-id="3c87f-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c87f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c87f-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c87f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c87f-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c87f-146">INPUTS</span></span>

### <span data-ttu-id="3c87f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3c87f-147">System.String</span></span>

### <span data-ttu-id="3c87f-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="3c87f-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="3c87f-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c87f-149">OUTPUTS</span></span>

### <span data-ttu-id="3c87f-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="3c87f-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="3c87f-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c87f-151">NOTES</span></span>

## <span data-ttu-id="3c87f-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c87f-152">RELATED LINKS</span></span>

[<span data-ttu-id="3c87f-153">Az U-SQL mostantól adatbázisszintű hozzáférés-vezérlést is kínál</span><span class="sxs-lookup"><span data-stu-id="3c87f-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="3c87f-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3c87f-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="3c87f-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3c87f-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
