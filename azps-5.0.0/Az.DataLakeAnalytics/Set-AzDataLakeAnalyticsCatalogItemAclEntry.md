---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: ab02a118eab993174261fc1a70c2dedbd6403d5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298013"
---
# <span data-ttu-id="797ae-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="797ae-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="797ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="797ae-102">SYNOPSIS</span></span>
<span data-ttu-id="797ae-103">Módosította az adattó-Analytics-katalógus vagy-katalógus egy bejegyzését az ACL-ben.</span><span class="sxs-lookup"><span data-stu-id="797ae-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="797ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="797ae-104">SYNTAX</span></span>

### <span data-ttu-id="797ae-105">SetCatalogAclEntryForUser (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="797ae-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="797ae-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="797ae-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="797ae-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="797ae-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="797ae-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="797ae-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="797ae-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="797ae-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="797ae-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="797ae-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="797ae-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="797ae-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="797ae-115">DESCRIPTION</span></span>
<span data-ttu-id="797ae-116">A **set-AzDataLakeAnalyticsCatalogItemAclEntry** parancsmag egy BEJEGYZÉST (ACE) ad hozzá vagy módosít egy katalógus vagy katalógus hozzáférés-vezérlési listájában (ACL) az adattó-elemzések listájában.</span><span class="sxs-lookup"><span data-stu-id="797ae-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="797ae-117">Példák</span><span class="sxs-lookup"><span data-stu-id="797ae-117">EXAMPLES</span></span>

### <span data-ttu-id="797ae-118">Példa 1: a katalógus felhasználói engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="797ae-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="797ae-119">Ez a parancs az írási engedélyekkel módosította az Patti Fuller katalógus ACE-t.</span><span class="sxs-lookup"><span data-stu-id="797ae-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="797ae-120">2. példa: az adatbázis felhasználói engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="797ae-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="797ae-121">Ez a parancs az az adatbázis-ACE for Patti Fuller-t módosítja az olvasási engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="797ae-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="797ae-122">3. példa: a katalógus egyéb engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="797ae-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="797ae-123">Ez a parancs a katalógus ACE-t módosította az olvasási engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="797ae-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="797ae-124">4. példa: az adatbázis egyéb engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="797ae-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="797ae-125">Példa 5: a felhasználói tulajdonosok engedélyeinek módosítása a katalógusban</span><span class="sxs-lookup"><span data-stu-id="797ae-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="797ae-126">Ez a parancs beállítja a fiók tulajdonosi engedélyét az olvasáshoz.</span><span class="sxs-lookup"><span data-stu-id="797ae-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="797ae-127">6. példa: az adatbázis felhasználói tulajdonosi engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="797ae-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="797ae-128">Ez a parancs beállítja az adatbázis tulajdonosi engedélyét az olvasáshoz.</span><span class="sxs-lookup"><span data-stu-id="797ae-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="797ae-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="797ae-129">PARAMETERS</span></span>

### <span data-ttu-id="797ae-130">-Fiók</span><span class="sxs-lookup"><span data-stu-id="797ae-130">-Account</span></span>
<span data-ttu-id="797ae-131">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="797ae-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="797ae-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="797ae-132">-DefaultProfile</span></span>
<span data-ttu-id="797ae-133">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="797ae-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="797ae-134">-Csoport</span><span class="sxs-lookup"><span data-stu-id="797ae-134">-Group</span></span>
<span data-ttu-id="797ae-135">Adja meg a katalógusfájl ACL-bejegyzését a csoport számára.</span><span class="sxs-lookup"><span data-stu-id="797ae-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="797ae-136">-GroupOwner</span></span>
<span data-ttu-id="797ae-137">ACL-bejegyzés beállítása a csoport tulajdonosának.</span><span class="sxs-lookup"><span data-stu-id="797ae-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="797ae-138">-ItemType</span></span>
<span data-ttu-id="797ae-139">A katalógus vagy a katalógus elem (ek) típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="797ae-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="797ae-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="797ae-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="797ae-141">Katalógus</span><span class="sxs-lookup"><span data-stu-id="797ae-141">Catalog</span></span>
- <span data-ttu-id="797ae-142">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="797ae-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="797ae-143">-ObjectId</span></span>
<span data-ttu-id="797ae-144">A beállítani kívánt felhasználó identitása.</span><span class="sxs-lookup"><span data-stu-id="797ae-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-145">– Egyéb</span><span class="sxs-lookup"><span data-stu-id="797ae-145">-Other</span></span>
<span data-ttu-id="797ae-146">Adja meg az ACL-bejegyzést a katalógushoz.</span><span class="sxs-lookup"><span data-stu-id="797ae-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-147">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="797ae-147">-Path</span></span>
<span data-ttu-id="797ae-148">Egy katalógus vagy katalógusfájl adattó-elemzési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="797ae-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="797ae-149">Az elérési út egyes részeit ponttal (.) kell elválasztani.</span><span class="sxs-lookup"><span data-stu-id="797ae-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-150">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="797ae-150">-Permissions</span></span>
<span data-ttu-id="797ae-151">Megadja az ACE-nek szóló engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="797ae-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="797ae-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="797ae-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="797ae-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="797ae-153">None</span></span>
- <span data-ttu-id="797ae-154">Olvasása</span><span class="sxs-lookup"><span data-stu-id="797ae-154">Read</span></span>
- <span data-ttu-id="797ae-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="797ae-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-156">-Felhasználó</span><span class="sxs-lookup"><span data-stu-id="797ae-156">-User</span></span>
<span data-ttu-id="797ae-157">A katalógus ACL-bejegyzésének beállítása a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="797ae-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="797ae-158">-UserOwner</span></span>
<span data-ttu-id="797ae-159">ACL-bejegyzés beállítása a felhasználó tulajdonosának.</span><span class="sxs-lookup"><span data-stu-id="797ae-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="797ae-160">-Confirm</span></span>
<span data-ttu-id="797ae-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="797ae-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="797ae-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="797ae-162">-WhatIf</span></span>
<span data-ttu-id="797ae-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="797ae-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="797ae-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="797ae-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="797ae-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797ae-165">CommonParameters</span></span>
<span data-ttu-id="797ae-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="797ae-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797ae-167">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="797ae-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797ae-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="797ae-168">INPUTS</span></span>

### <span data-ttu-id="797ae-169">System. String</span><span class="sxs-lookup"><span data-stu-id="797ae-169">System.String</span></span>

### <span data-ttu-id="797ae-170">System. GUID</span><span class="sxs-lookup"><span data-stu-id="797ae-170">System.Guid</span></span>

### <span data-ttu-id="797ae-171">Microsoft. Azure. Command. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="797ae-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="797ae-172">Microsoft. Azure. Command. DataLakeAnalytics. modellek. DataLakeAnalyticsEnums + PermissionType</span><span class="sxs-lookup"><span data-stu-id="797ae-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="797ae-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="797ae-173">OUTPUTS</span></span>

### <span data-ttu-id="797ae-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="797ae-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="797ae-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="797ae-175">NOTES</span></span>

## <span data-ttu-id="797ae-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="797ae-176">RELATED LINKS</span></span>

[<span data-ttu-id="797ae-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="797ae-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="797ae-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="797ae-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="797ae-179">Az U-SQL most az adatbázis szintű hozzáférés-vezérlést kínálja</span><span class="sxs-lookup"><span data-stu-id="797ae-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
