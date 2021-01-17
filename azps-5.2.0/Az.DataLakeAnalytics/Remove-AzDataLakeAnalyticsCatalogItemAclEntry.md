---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 8b227d16a55d1e5f92c6021099a01b9df5550bd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372874"
---
# <span data-ttu-id="d2479-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d2479-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="d2479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2479-102">SYNOPSIS</span></span>
<span data-ttu-id="d2479-103">A Data Lake Analytics szolgáltatás katalógus- vagy katalóguselemének ACL-ének bejegyzését törli.</span><span class="sxs-lookup"><span data-stu-id="d2479-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="d2479-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2479-104">SYNTAX</span></span>

### <span data-ttu-id="d2479-105">RemoveCatalogAclEntryForUser (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2479-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2479-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="d2479-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2479-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="d2479-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2479-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="d2479-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2479-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2479-109">DESCRIPTION</span></span>
<span data-ttu-id="d2479-110">A **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** parancsmag eltávolít egy bejegyzést a Data Lake Analytics szolgáltatásban található katalógus vagy katalóguselem hozzáférés-vezérlési listájából (ACL).</span><span class="sxs-lookup"><span data-stu-id="d2479-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="d2479-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2479-111">EXAMPLES</span></span>

### <span data-ttu-id="d2479-112">1. példa: Katalógus felhasználói ACL-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d2479-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="d2479-113">Ez a parancs eltávolítja a contosoadla-fiók Patti Fuller katalógusának ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="d2479-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="d2479-114">2. példa: Adatbázis felhasználói ACL-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d2479-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="d2479-115">Ez a parancs eltávolítja a contosoadla-fiók Patti Fuller adatbázisának ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="d2479-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="d2479-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2479-116">PARAMETERS</span></span>

### <span data-ttu-id="d2479-117">-Account</span><span class="sxs-lookup"><span data-stu-id="d2479-117">-Account</span></span>
<span data-ttu-id="d2479-118">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2479-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d2479-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2479-119">-DefaultProfile</span></span>
<span data-ttu-id="d2479-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2479-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2479-121">-Group</span><span class="sxs-lookup"><span data-stu-id="d2479-121">-Group</span></span>
<span data-ttu-id="d2479-122">Csoport katalógusának ACL-bejegyzésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d2479-122">Remove ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="d2479-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="d2479-123">-ItemType</span></span>
<span data-ttu-id="d2479-124">A katalógus vagy katalóguselem(ök) típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d2479-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="d2479-125">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="d2479-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2479-126">Katalógus</span><span class="sxs-lookup"><span data-stu-id="d2479-126">Catalog</span></span>
- <span data-ttu-id="d2479-127">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="d2479-127">Database</span></span>

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

### <span data-ttu-id="d2479-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d2479-128">-ObjectId</span></span>
<span data-ttu-id="d2479-129">Az eltávolítható felhasználó identitása.</span><span class="sxs-lookup"><span data-stu-id="d2479-129">The identity of the user to remove.</span></span>

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

### <span data-ttu-id="d2479-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2479-130">-PassThru</span></span>
<span data-ttu-id="d2479-131">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="d2479-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d2479-132">-Path</span><span class="sxs-lookup"><span data-stu-id="d2479-132">-Path</span></span>
<span data-ttu-id="d2479-133">Egy katalógus vagy katalóguselem Data Lake Analytics-útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2479-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="d2479-134">Az elérési út egyes részeit pont (.) választja el egymástól.</span><span class="sxs-lookup"><span data-stu-id="d2479-134">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="d2479-135">-Felhasználó</span><span class="sxs-lookup"><span data-stu-id="d2479-135">-User</span></span>
<span data-ttu-id="d2479-136">Felhasználó katalógusának ACL-bejegyzésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d2479-136">Remove ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="d2479-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2479-137">-Confirm</span></span>
<span data-ttu-id="d2479-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d2479-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2479-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2479-139">-WhatIf</span></span>
<span data-ttu-id="d2479-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d2479-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2479-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2479-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2479-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2479-142">CommonParameters</span></span>
<span data-ttu-id="d2479-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2479-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2479-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2479-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2479-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2479-145">INPUTS</span></span>

### <span data-ttu-id="d2479-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d2479-146">System.String</span></span>

### <span data-ttu-id="d2479-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d2479-147">System.Guid</span></span>

### <span data-ttu-id="d2479-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="d2479-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="d2479-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2479-149">OUTPUTS</span></span>

### <span data-ttu-id="d2479-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2479-150">System.Boolean</span></span>

## <span data-ttu-id="d2479-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2479-151">NOTES</span></span>

## <span data-ttu-id="d2479-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2479-152">RELATED LINKS</span></span>

[<span data-ttu-id="d2479-153">Az U-SQL mostantól adatbázisszintű hozzáférés-vezérlést is kínál</span><span class="sxs-lookup"><span data-stu-id="d2479-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="d2479-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d2479-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="d2479-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d2479-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
