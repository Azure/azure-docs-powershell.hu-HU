---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8bef754d7d9020193e4694953222a6579341c9ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480452"
---
# <span data-ttu-id="792a8-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="792a8-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="792a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="792a8-102">SYNOPSIS</span></span>
<span data-ttu-id="792a8-103">Frissíti egy eszköz megosztási részét.</span><span class="sxs-lookup"><span data-stu-id="792a8-103">Updates the share for a device.</span></span>

## <span data-ttu-id="792a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="792a8-104">SYNTAX</span></span>

### <span data-ttu-id="792a8-105">SmbParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="792a8-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="792a8-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="792a8-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792a8-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="792a8-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792a8-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="792a8-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792a8-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="792a8-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792a8-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="792a8-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="792a8-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="792a8-111">DESCRIPTION</span></span>
<span data-ttu-id="792a8-112">Ez a **Set-AzDataBoxEdgeShare** lecseréli a hozzáférési jogokat</span><span class="sxs-lookup"><span data-stu-id="792a8-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="792a8-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="792a8-113">EXAMPLES</span></span>

### <span data-ttu-id="792a8-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="792a8-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="792a8-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="792a8-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="792a8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="792a8-116">PARAMETERS</span></span>

### <span data-ttu-id="792a8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="792a8-117">-AsJob</span></span>
<span data-ttu-id="792a8-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="792a8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="792a8-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="792a8-119">-ClientAccessRight</span></span>
<span data-ttu-id="792a8-120">Olvasható/írhatja az Accesst ügyfélazonosítókhoz, például:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="792a8-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792a8-121">-DefaultProfile</span></span>
<span data-ttu-id="792a8-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="792a8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792a8-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="792a8-123">-DeviceName</span></span>
<span data-ttu-id="792a8-124">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="792a8-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792a8-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="792a8-125">-InputObject</span></span>
<span data-ttu-id="792a8-126">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="792a8-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="792a8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="792a8-127">-Name</span></span>
<span data-ttu-id="792a8-128">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="792a8-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792a8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792a8-129">-ResourceGroupName</span></span>
<span data-ttu-id="792a8-130">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="792a8-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792a8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="792a8-131">-ResourceId</span></span>
<span data-ttu-id="792a8-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="792a8-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792a8-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="792a8-133">-UserAccessRight</span></span>
<span data-ttu-id="792a8-134">biztosítson hozzáférést közvetlenül a meglévő felhasználónévvel együtt az SMB megosztási típusainak eléréséhez, például: @(@{"Felhasználónév"="felhasználónév-1";" AccessRight"="Read"}, @{"Felhasználónév"="felhasználónév-2";" AccessRight"="Read"}, @{"Felhasználónév"="felhasználónév-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="792a8-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792a8-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="792a8-135">-Confirm</span></span>
<span data-ttu-id="792a8-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="792a8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="792a8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="792a8-137">-WhatIf</span></span>
<span data-ttu-id="792a8-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="792a8-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="792a8-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="792a8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="792a8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792a8-140">CommonParameters</span></span>
<span data-ttu-id="792a8-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="792a8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792a8-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="792a8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792a8-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="792a8-143">INPUTS</span></span>

### <span data-ttu-id="792a8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="792a8-144">System.String</span></span>

### <span data-ttu-id="792a8-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="792a8-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="792a8-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="792a8-146">OUTPUTS</span></span>

### <span data-ttu-id="792a8-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="792a8-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="792a8-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="792a8-148">NOTES</span></span>

## <span data-ttu-id="792a8-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="792a8-149">RELATED LINKS</span></span>
