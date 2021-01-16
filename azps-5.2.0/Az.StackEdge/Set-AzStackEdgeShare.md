---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325174"
---
# <span data-ttu-id="6d3cf-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6d3cf-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="6d3cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3cf-103">Frissíti egy eszköz megosztási részét.</span><span class="sxs-lookup"><span data-stu-id="6d3cf-103">Updates the share for a device.</span></span>

## <span data-ttu-id="6d3cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d3cf-104">SYNTAX</span></span>

### <span data-ttu-id="6d3cf-105">SmbParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d3cf-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d3cf-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d3cf-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d3cf-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d3cf-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d3cf-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d3cf-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d3cf-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d3cf-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d3cf-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d3cf-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d3cf-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d3cf-111">DESCRIPTION</span></span>
<span data-ttu-id="6d3cf-112">Ez a **Set-AzStackEdgeShare** lecseréli a hozzáférési jogokat</span><span class="sxs-lookup"><span data-stu-id="6d3cf-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="6d3cf-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d3cf-113">EXAMPLES</span></span>

### <span data-ttu-id="6d3cf-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="6d3cf-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="6d3cf-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="6d3cf-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="6d3cf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d3cf-116">PARAMETERS</span></span>

### <span data-ttu-id="6d3cf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d3cf-117">-AsJob</span></span>
<span data-ttu-id="6d3cf-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6d3cf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d3cf-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="6d3cf-119">-ClientAccessRight</span></span>
<span data-ttu-id="6d3cf-120">Olvasható/írhatja az Accesst az ügyfélazonosítókhoz, például:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="6d3cf-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="6d3cf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3cf-121">-DefaultProfile</span></span>
<span data-ttu-id="6d3cf-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d3cf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d3cf-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6d3cf-123">-DeviceName</span></span>
<span data-ttu-id="6d3cf-124">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="6d3cf-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3cf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d3cf-125">-InputObject</span></span>
<span data-ttu-id="6d3cf-126">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="6d3cf-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3cf-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6d3cf-127">-Name</span></span>
<span data-ttu-id="6d3cf-128">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="6d3cf-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3cf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d3cf-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d3cf-130">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6d3cf-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3cf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d3cf-131">-ResourceId</span></span>
<span data-ttu-id="6d3cf-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d3cf-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="6d3cf-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="6d3cf-133">-UserAccessRight</span></span>
<span data-ttu-id="6d3cf-134">biztosítson hozzáférést közvetlenül a meglévő felhasználónévvel együtt az SMB megosztási típusainak eléréséhez, például: @(@{"Felhasználónév"="felhasználónév-1";" AccessRight"="Read"}, @{"Felhasználónév"="felhasználónév-2";" AccessRight"="Read"}, @{"Felhasználónév"="felhasználónév-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="6d3cf-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="6d3cf-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d3cf-135">-Confirm</span></span>
<span data-ttu-id="6d3cf-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d3cf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d3cf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d3cf-137">-WhatIf</span></span>
<span data-ttu-id="6d3cf-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d3cf-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d3cf-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d3cf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d3cf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3cf-140">CommonParameters</span></span>
<span data-ttu-id="6d3cf-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d3cf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3cf-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d3cf-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3cf-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d3cf-143">INPUTS</span></span>

### <span data-ttu-id="6d3cf-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6d3cf-144">System.String</span></span>

### <span data-ttu-id="6d3cf-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6d3cf-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="6d3cf-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d3cf-146">OUTPUTS</span></span>

### <span data-ttu-id="6d3cf-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6d3cf-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="6d3cf-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d3cf-148">NOTES</span></span>

## <span data-ttu-id="6d3cf-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d3cf-149">RELATED LINKS</span></span>
