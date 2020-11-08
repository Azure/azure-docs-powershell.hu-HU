---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187199"
---
# <span data-ttu-id="b7a36-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b7a36-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="b7a36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7a36-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a36-103">Frissíti az eszköz megosztását.</span><span class="sxs-lookup"><span data-stu-id="b7a36-103">Updates the share for a device.</span></span>

## <span data-ttu-id="b7a36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7a36-104">SYNTAX</span></span>

### <span data-ttu-id="b7a36-105">SmbParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7a36-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7a36-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a36-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7a36-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a36-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7a36-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a36-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7a36-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a36-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7a36-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a36-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7a36-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7a36-111">DESCRIPTION</span></span>
<span data-ttu-id="b7a36-112">Ez a **set-AzStackEdgeShare** a hozzáférési jogokat fogja lecserélni.</span><span class="sxs-lookup"><span data-stu-id="b7a36-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="b7a36-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b7a36-113">EXAMPLES</span></span>

### <span data-ttu-id="b7a36-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7a36-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="b7a36-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="b7a36-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="b7a36-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7a36-116">PARAMETERS</span></span>

### <span data-ttu-id="b7a36-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7a36-117">-AsJob</span></span>
<span data-ttu-id="b7a36-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b7a36-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7a36-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="b7a36-119">-ClientAccessRight</span></span>
<span data-ttu-id="b7a36-120">Olvasási/írási hozzáférés a clientIds-hoz, például: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" nem érhető el "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="b7a36-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="b7a36-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a36-121">-DefaultProfile</span></span>
<span data-ttu-id="b7a36-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7a36-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7a36-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b7a36-123">-DeviceName</span></span>
<span data-ttu-id="b7a36-124">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="b7a36-124">Device Name</span></span>

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

### <span data-ttu-id="b7a36-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7a36-125">-InputObject</span></span>
<span data-ttu-id="b7a36-126">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="b7a36-126">Input Object</span></span>

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

### <span data-ttu-id="b7a36-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7a36-127">-Name</span></span>
<span data-ttu-id="b7a36-128">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b7a36-128">Resource Name</span></span>

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

### <span data-ttu-id="b7a36-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a36-129">-ResourceGroupName</span></span>
<span data-ttu-id="b7a36-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b7a36-130">Resource Group Name</span></span>

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

### <span data-ttu-id="b7a36-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7a36-131">-ResourceId</span></span>
<span data-ttu-id="b7a36-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7a36-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="b7a36-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="b7a36-133">-UserAccessRight</span></span>
<span data-ttu-id="b7a36-134">hozzáférés biztosítása a meglévő felhasználónévekkel együtt az SMB-megosztási típusok eléréséhez, például: @ (@ {"username" = "User-1"; " AccessRight "=" READ "}, @ {" username "=" User-Name-2 ";" AccessRight "=" READ "}, @ {" username "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="b7a36-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="b7a36-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7a36-135">-Confirm</span></span>
<span data-ttu-id="b7a36-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7a36-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7a36-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a36-137">-WhatIf</span></span>
<span data-ttu-id="b7a36-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7a36-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7a36-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7a36-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7a36-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a36-140">CommonParameters</span></span>
<span data-ttu-id="b7a36-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7a36-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a36-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b7a36-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a36-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7a36-143">INPUTS</span></span>

### <span data-ttu-id="b7a36-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b7a36-144">System.String</span></span>

### <span data-ttu-id="b7a36-145">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b7a36-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="b7a36-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7a36-146">OUTPUTS</span></span>

### <span data-ttu-id="b7a36-147">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b7a36-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="b7a36-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7a36-148">NOTES</span></span>

## <span data-ttu-id="b7a36-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7a36-149">RELATED LINKS</span></span>
