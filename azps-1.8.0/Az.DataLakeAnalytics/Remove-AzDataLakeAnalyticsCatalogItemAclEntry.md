---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 6d30985baed220ee4a7a599f1214c0c4124ef08d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836386"
---
# <span data-ttu-id="0b3e7-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b3e7-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="0b3e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b3e7-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3e7-103">Töröl egy bejegyzést az adattó-elemzési katalógusból vagy katalógusból származó elemről.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="0b3e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b3e7-104">SYNTAX</span></span>

### <span data-ttu-id="0b3e7-105">RemoveCatalogAclEntryForUser (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b3e7-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b3e7-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="0b3e7-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b3e7-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="0b3e7-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b3e7-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="0b3e7-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b3e7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b3e7-109">DESCRIPTION</span></span>
<span data-ttu-id="0b3e7-110">A **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** parancsmag egy bejegyzés (ACE) eltávolítását tartalmazza egy katalógus vagy katalógus hozzáférés-vezérlési listájából (ACL) az adattó-Analytics szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="0b3e7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0b3e7-111">EXAMPLES</span></span>

### <span data-ttu-id="0b3e7-112">1. példa: a felhasználó ACL-je eltávolítása a katalógushoz</span><span class="sxs-lookup"><span data-stu-id="0b3e7-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="0b3e7-113">Ez a parancs eltávolítja a katalógus-ACL-t az contosoadla-fiókhoz tartozó Patti Fuller számára.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="0b3e7-114">2. példa: az adatbázis felhasználó ACL-je eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0b3e7-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="0b3e7-115">Ez a parancs eltávolítja a contosoadla-fiók adatbázis-hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="0b3e7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b3e7-116">PARAMETERS</span></span>

### <span data-ttu-id="0b3e7-117">-Fiók</span><span class="sxs-lookup"><span data-stu-id="0b3e7-117">-Account</span></span>
<span data-ttu-id="0b3e7-118">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0b3e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3e7-119">-DefaultProfile</span></span>
<span data-ttu-id="0b3e7-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b3e7-121">-Csoport</span><span class="sxs-lookup"><span data-stu-id="0b3e7-121">-Group</span></span>
<span data-ttu-id="0b3e7-122">Távolítsa el a termékkatalógus ACL-bejegyzését a csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e7-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="0b3e7-123">-ItemType</span></span>
<span data-ttu-id="0b3e7-124">A katalógus vagy a katalógus elem (ek) típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="0b3e7-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b3e7-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b3e7-126">Katalógus</span><span class="sxs-lookup"><span data-stu-id="0b3e7-126">Catalog</span></span>
- <span data-ttu-id="0b3e7-127">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="0b3e7-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e7-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0b3e7-128">-ObjectId</span></span>
<span data-ttu-id="0b3e7-129">Az eltávolítandó felhasználó identitása.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e7-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b3e7-130">-PassThru</span></span>
<span data-ttu-id="0b3e7-131">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="0b3e7-132">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0b3e7-132">-Path</span></span>
<span data-ttu-id="0b3e7-133">Egy katalógus vagy katalógusfájl adattó-elemzési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="0b3e7-134">Az elérési út egyes részeit ponttal (.) kell elválasztani.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e7-135">-Felhasználó</span><span class="sxs-lookup"><span data-stu-id="0b3e7-135">-User</span></span>
<span data-ttu-id="0b3e7-136">A katalógus ACL-bejegyzésének eltávolítása a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e7-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0b3e7-137">-Confirm</span></span>
<span data-ttu-id="0b3e7-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b3e7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3e7-139">-WhatIf</span></span>
<span data-ttu-id="0b3e7-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b3e7-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0b3e7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b3e7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3e7-142">CommonParameters</span></span>
<span data-ttu-id="0b3e7-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b3e7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3e7-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3e7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3e7-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b3e7-145">INPUTS</span></span>

### <span data-ttu-id="0b3e7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0b3e7-146">System.String</span></span>

### <span data-ttu-id="0b3e7-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0b3e7-147">System.Guid</span></span>

### <span data-ttu-id="0b3e7-148">Microsoft. Azure. Command. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="0b3e7-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="0b3e7-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b3e7-149">OUTPUTS</span></span>

### <span data-ttu-id="0b3e7-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b3e7-150">System.Boolean</span></span>

## <span data-ttu-id="0b3e7-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b3e7-151">NOTES</span></span>

## <span data-ttu-id="0b3e7-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b3e7-152">RELATED LINKS</span></span>

[<span data-ttu-id="0b3e7-153">Az U-SQL most az adatbázis szintű hozzáférés-vezérlést kínálja</span><span class="sxs-lookup"><span data-stu-id="0b3e7-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="0b3e7-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b3e7-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="0b3e7-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b3e7-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
