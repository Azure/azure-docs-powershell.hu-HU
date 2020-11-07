---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac4f7814898bcbfcee75c4a31273dfbcb6be7335
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842402"
---
# <span data-ttu-id="9cc49-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="9cc49-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="9cc49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cc49-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc49-103">Frissíti az eszköz megosztását.</span><span class="sxs-lookup"><span data-stu-id="9cc49-103">Updates the share for a device.</span></span>

## <span data-ttu-id="9cc49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cc49-104">SYNTAX</span></span>

### <span data-ttu-id="9cc49-105">SmbParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cc49-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cc49-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cc49-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc49-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cc49-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc49-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cc49-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc49-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cc49-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc49-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cc49-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cc49-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cc49-111">DESCRIPTION</span></span>
<span data-ttu-id="9cc49-112">Ez a **set-AzDataBoxEdgeShare** a hozzáférési jogokat fogja lecserélni.</span><span class="sxs-lookup"><span data-stu-id="9cc49-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="9cc49-113">Példák</span><span class="sxs-lookup"><span data-stu-id="9cc49-113">EXAMPLES</span></span>

### <span data-ttu-id="9cc49-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9cc49-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="9cc49-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="9cc49-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="9cc49-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cc49-116">PARAMETERS</span></span>

### <span data-ttu-id="9cc49-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cc49-117">-AsJob</span></span>
<span data-ttu-id="9cc49-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9cc49-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cc49-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="9cc49-119">-ClientAccessRight</span></span>
<span data-ttu-id="9cc49-120">Olvasási/írási hozzáférés a clientIds-hoz, például: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" nem érhető el "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="9cc49-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="9cc49-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc49-121">-DefaultProfile</span></span>
<span data-ttu-id="9cc49-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cc49-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cc49-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9cc49-123">-DeviceName</span></span>
<span data-ttu-id="9cc49-124">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="9cc49-124">Device Name</span></span>

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

### <span data-ttu-id="9cc49-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cc49-125">-InputObject</span></span>
<span data-ttu-id="9cc49-126">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="9cc49-126">Input Object</span></span>

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

### <span data-ttu-id="9cc49-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9cc49-127">-Name</span></span>
<span data-ttu-id="9cc49-128">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="9cc49-128">Resource Name</span></span>

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

### <span data-ttu-id="9cc49-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc49-129">-ResourceGroupName</span></span>
<span data-ttu-id="9cc49-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9cc49-130">Resource Group Name</span></span>

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

### <span data-ttu-id="9cc49-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cc49-131">-ResourceId</span></span>
<span data-ttu-id="9cc49-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cc49-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="9cc49-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="9cc49-133">-UserAccessRight</span></span>
<span data-ttu-id="9cc49-134">hozzáférés biztosítása a meglévő felhasználónévekkel együtt az SMB-megosztási típusok eléréséhez, például: @ (@ {"username" = "User-1"; " AccessRight "=" READ "}, @ {" username "=" User-Name-2 ";" AccessRight "=" READ "}, @ {" username "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="9cc49-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="9cc49-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9cc49-135">-Confirm</span></span>
<span data-ttu-id="9cc49-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9cc49-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc49-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc49-137">-WhatIf</span></span>
<span data-ttu-id="9cc49-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9cc49-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cc49-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cc49-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc49-140">CommonParameters</span></span>
<span data-ttu-id="9cc49-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cc49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc49-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9cc49-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc49-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc49-143">INPUTS</span></span>

### <span data-ttu-id="9cc49-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9cc49-144">System.String</span></span>

### <span data-ttu-id="9cc49-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="9cc49-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="9cc49-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc49-146">OUTPUTS</span></span>

### <span data-ttu-id="9cc49-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="9cc49-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="9cc49-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cc49-148">NOTES</span></span>

## <span data-ttu-id="9cc49-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cc49-149">RELATED LINKS</span></span>
