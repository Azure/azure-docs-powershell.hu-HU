---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: ab02a118eab993174261fc1a70c2dedbd6403d5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161994"
---
# <span data-ttu-id="c2fb7-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c2fb7-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="c2fb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fb7-103">Módosít egy bejegyzést a Data Lake Analytics katalógus- vagy katalóguselemének ACL-ében.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="c2fb7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2fb7-104">SYNTAX</span></span>

### <span data-ttu-id="c2fb7-105">SetCatalogAclEntryForUser (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2fb7-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="c2fb7-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="c2fb7-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="c2fb7-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="c2fb7-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="c2fb7-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="c2fb7-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="c2fb7-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="c2fb7-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fb7-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="c2fb7-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2fb7-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2fb7-115">DESCRIPTION</span></span>
<span data-ttu-id="c2fb7-116">A **Set-AzDataLakeAnalyticsCatalogItemAclEntry** parancsmag hozzáad vagy módosít egy bejegyzést (ACE) egy katalógus vagy katalóguselem hozzáférés-vezérlési listájában (ACL) a Data Lake Analytics szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="c2fb7-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2fb7-117">EXAMPLES</span></span>

### <span data-ttu-id="c2fb7-118">1. példa: A katalógus felhasználói engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="c2fb7-119">Ez a parancs módosítja a Patti Fuller-hez tartozó ACE katalógust olvasási engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="c2fb7-120">2. példa: Adatbázis felhasználói engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="c2fb7-121">Ez a parancs olvasási engedélyekkel módosítja Patti Fuller számára az ACE-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="c2fb7-122">3. példa: Katalógus egyéb engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="c2fb7-123">Ez a parancs módosítja az ACE-katalógust más számára olvasási engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="c2fb7-124">4. példa: Adatbázis egyéb engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="c2fb7-125">5. példa: A katalógus felhasználói tulajdonosi engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="c2fb7-126">Ez a parancs olvasásra állítja a fiók tulajdonosi engedélyét.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="c2fb7-127">6. példa: Adatbázis felhasználói tulajdonosi engedélyeinek módosítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="c2fb7-128">Ez a parancs olvasásra állítja az adatbázis tulajdonosi engedélyét.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="c2fb7-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2fb7-129">PARAMETERS</span></span>

### <span data-ttu-id="c2fb7-130">-Account</span><span class="sxs-lookup"><span data-stu-id="c2fb7-130">-Account</span></span>
<span data-ttu-id="c2fb7-131">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c2fb7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fb7-132">-DefaultProfile</span></span>
<span data-ttu-id="c2fb7-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2fb7-134">-Group</span><span class="sxs-lookup"><span data-stu-id="c2fb7-134">-Group</span></span>
<span data-ttu-id="c2fb7-135">Csoport katalógusának ACL-bejegyzésének beállítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-135">Set ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="c2fb7-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="c2fb7-136">-GroupOwner</span></span>
<span data-ttu-id="c2fb7-137">Set ACL entry of catalog for group owner.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-137">Set ACL entry of catalog for group owner.</span></span>

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

### <span data-ttu-id="c2fb7-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="c2fb7-138">-ItemType</span></span>
<span data-ttu-id="c2fb7-139">A katalógus vagy katalóguselem(ök) típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="c2fb7-140">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="c2fb7-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2fb7-141">Katalógus</span><span class="sxs-lookup"><span data-stu-id="c2fb7-141">Catalog</span></span>
- <span data-ttu-id="c2fb7-142">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="c2fb7-142">Database</span></span>

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

### <span data-ttu-id="c2fb7-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c2fb7-143">-ObjectId</span></span>
<span data-ttu-id="c2fb7-144">A beállított felhasználó identitása.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-144">The identity of the user to set.</span></span>

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

### <span data-ttu-id="c2fb7-145">-Egyéb</span><span class="sxs-lookup"><span data-stu-id="c2fb7-145">-Other</span></span>
<span data-ttu-id="c2fb7-146">Más típusú katalógus ACL-bejegyzésének beállítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-146">Set ACL entry of catalog for other.</span></span>

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

### <span data-ttu-id="c2fb7-147">-Path</span><span class="sxs-lookup"><span data-stu-id="c2fb7-147">-Path</span></span>
<span data-ttu-id="c2fb7-148">Egy katalógus vagy katalóguselem Data Lake Analytics-útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="c2fb7-149">Az elérési út részeit pont (.) választja el egymástól.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-149">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="c2fb7-150">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="c2fb7-150">-Permissions</span></span>
<span data-ttu-id="c2fb7-151">Az ACE engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="c2fb7-152">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="c2fb7-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2fb7-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="c2fb7-153">None</span></span>
- <span data-ttu-id="c2fb7-154">Olvasás</span><span class="sxs-lookup"><span data-stu-id="c2fb7-154">Read</span></span>
- <span data-ttu-id="c2fb7-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2fb7-155">ReadWrite</span></span>

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

### <span data-ttu-id="c2fb7-156">-Felhasználó</span><span class="sxs-lookup"><span data-stu-id="c2fb7-156">-User</span></span>
<span data-ttu-id="c2fb7-157">A felhasználó katalógusának ACL-bejegyzésének beállítása</span><span class="sxs-lookup"><span data-stu-id="c2fb7-157">Set ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="c2fb7-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="c2fb7-158">-UserOwner</span></span>
<span data-ttu-id="c2fb7-159">Set ACL entry of catalog for user owner.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-159">Set ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="c2fb7-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2fb7-160">-Confirm</span></span>
<span data-ttu-id="c2fb7-161">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2fb7-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2fb7-162">-WhatIf</span></span>
<span data-ttu-id="c2fb7-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2fb7-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2fb7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fb7-165">CommonParameters</span></span>
<span data-ttu-id="c2fb7-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fb7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fb7-167">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2fb7-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fb7-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2fb7-168">INPUTS</span></span>

### <span data-ttu-id="c2fb7-169">System.String</span><span class="sxs-lookup"><span data-stu-id="c2fb7-169">System.String</span></span>

### <span data-ttu-id="c2fb7-170">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c2fb7-170">System.Guid</span></span>

### <span data-ttu-id="c2fb7-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="c2fb7-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="c2fb7-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span><span class="sxs-lookup"><span data-stu-id="c2fb7-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="c2fb7-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2fb7-173">OUTPUTS</span></span>

### <span data-ttu-id="c2fb7-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="c2fb7-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="c2fb7-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2fb7-175">NOTES</span></span>

## <span data-ttu-id="c2fb7-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2fb7-176">RELATED LINKS</span></span>

[<span data-ttu-id="c2fb7-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c2fb7-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="c2fb7-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c2fb7-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="c2fb7-179">Az U-SQL mostantól adatbázisszintű hozzáférés-vezérlést is kínál</span><span class="sxs-lookup"><span data-stu-id="c2fb7-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
