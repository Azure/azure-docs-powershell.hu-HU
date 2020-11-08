---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 134a236a8259a3197abed3b033c86904a9389643
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182831"
---
# <span data-ttu-id="cb2a0-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cb2a0-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="cb2a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2a0-103">Megadhat egy bejegyzést az adattó-elemzési katalógus vagy katalógus elemeinek hozzáférés-vezérlési területén.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="cb2a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb2a0-104">SYNTAX</span></span>

### <span data-ttu-id="cb2a0-105">GetCatalogAclEntry (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb2a0-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb2a0-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="cb2a0-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2a0-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="cb2a0-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2a0-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cb2a0-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2a0-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="cb2a0-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2a0-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="cb2a0-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb2a0-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb2a0-111">DESCRIPTION</span></span>
<span data-ttu-id="cb2a0-112">A **Get-AzDataLakeAnalyticsCatalogItemAclEntry** parancsmag az adattó-elemzések katalógusa vagy katalógusa hozzáférés-vezérlési listájában (ACE) tartalmazza a bejegyzések (ACE-EK) listáját.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="cb2a0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="cb2a0-113">EXAMPLES</span></span>

### <span data-ttu-id="cb2a0-114">Példa 1: a katalógushoz tartozó hozzáférés-vezérlési lista beszerzése</span><span class="sxs-lookup"><span data-stu-id="cb2a0-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="cb2a0-115">Ez a parancs beilleszti a megadott adattó-fiók katalógusának hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="cb2a0-116">2. példa: a felhasználó hozzáférés-vezérlési bejegyzésének beszerzése egy katalógusban</span><span class="sxs-lookup"><span data-stu-id="cb2a0-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="cb2a0-117">Ez a parancs beolvassa a felhasználó tulajdonosának ACL-bejegyzését a megadott adat-tó Analytics-fiókja katalógusához.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="cb2a0-118">Példa: a csoport tulajdonosának hozzáférés-vezérlési bejegyzésének beszerzése katalógushoz</span><span class="sxs-lookup"><span data-stu-id="cb2a0-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="cb2a0-119">Ez a parancs beilleszti a csoport tulajdonosának hozzáférés-vezérlési bejegyzését a megadott adat-tó Analytics-fiókja katalógusához.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="cb2a0-120">Példa 4: az adatbázis-hozzáférés-vezérlés beszerzése</span><span class="sxs-lookup"><span data-stu-id="cb2a0-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="cb2a0-121">Ez a parancs beilleszti a megadott Data Lake Analytics-fiók adatbázisának hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="cb2a0-122">Példa 5: az adatbázis felhasználói tulajdonosának hozzáférés-vezérlési bejegyzésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="cb2a0-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="cb2a0-123">Ez a parancs beilleszti a felhasználó tulajdonosának hozzáférés-vezérlési bejegyzését a megadott adattó-alapú adatkezelési fiók adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="cb2a0-124">Példa 6: a csoport tulajdonosának hozzáférés-vezérlési bejegyzésének beszerzése egy adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="cb2a0-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="cb2a0-125">Ez a parancs beolvassa a csoport tulajdonosának hozzáférés-vezérlési bejegyzését a megadott adattó Analytics-fiók adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="cb2a0-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb2a0-126">PARAMETERS</span></span>

### <span data-ttu-id="cb2a0-127">-Fiók</span><span class="sxs-lookup"><span data-stu-id="cb2a0-127">-Account</span></span>
<span data-ttu-id="cb2a0-128">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cb2a0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2a0-129">-DefaultProfile</span></span>
<span data-ttu-id="cb2a0-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb2a0-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="cb2a0-131">-GroupOwner</span></span>
<span data-ttu-id="cb2a0-132">A katalógus ACL-bejegyzésének beszerzése a csoport tulajdonosai számára</span><span class="sxs-lookup"><span data-stu-id="cb2a0-132">Get ACL entry of catalog for group owner</span></span>

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

### <span data-ttu-id="cb2a0-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="cb2a0-133">-ItemType</span></span>
<span data-ttu-id="cb2a0-134">A katalógus vagy a katalógus elem (ek) típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="cb2a0-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cb2a0-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb2a0-136">Katalógus</span><span class="sxs-lookup"><span data-stu-id="cb2a0-136">Catalog</span></span>
- <span data-ttu-id="cb2a0-137">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="cb2a0-137">Database</span></span>

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

### <span data-ttu-id="cb2a0-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="cb2a0-138">-Path</span></span>
<span data-ttu-id="cb2a0-139">Egy katalógus vagy katalógusfájl adattó-elemzési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="cb2a0-140">Az elérési út egyes részeit ponttal (.) kell elválasztani.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-140">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="cb2a0-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="cb2a0-141">-UserOwner</span></span>
<span data-ttu-id="cb2a0-142">ACL-bejegyzés kérése a felhasználó tulajdonosának.</span><span class="sxs-lookup"><span data-stu-id="cb2a0-142">Get ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="cb2a0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2a0-143">CommonParameters</span></span>
<span data-ttu-id="cb2a0-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb2a0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2a0-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2a0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2a0-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2a0-146">INPUTS</span></span>

### <span data-ttu-id="cb2a0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="cb2a0-147">System.String</span></span>

### <span data-ttu-id="cb2a0-148">Microsoft. Azure. Command. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="cb2a0-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="cb2a0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2a0-149">OUTPUTS</span></span>

### <span data-ttu-id="cb2a0-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="cb2a0-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="cb2a0-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb2a0-151">NOTES</span></span>

## <span data-ttu-id="cb2a0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb2a0-152">RELATED LINKS</span></span>

[<span data-ttu-id="cb2a0-153">Az U-SQL most az adatbázis szintű hozzáférés-vezérlést kínálja</span><span class="sxs-lookup"><span data-stu-id="cb2a0-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="cb2a0-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cb2a0-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="cb2a0-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cb2a0-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
