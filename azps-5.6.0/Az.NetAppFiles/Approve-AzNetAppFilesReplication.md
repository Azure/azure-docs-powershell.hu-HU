---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: ac562f95ad6d5cbc97e31cd3832b90d2aa2362e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926962"
---
# <span data-ttu-id="d7997-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="d7997-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="d7997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7997-102">SYNOPSIS</span></span>
<span data-ttu-id="d7997-103">Replikációs kapcsolat jóváhagyása/jóváhagyása a forrásköteten</span><span class="sxs-lookup"><span data-stu-id="d7997-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="d7997-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7997-104">SYNTAX</span></span>

### <span data-ttu-id="d7997-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7997-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7997-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7997-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7997-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7997-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7997-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7997-108">DESCRIPTION</span></span>
<span data-ttu-id="d7997-109">A forráskötet replikációs kapcsolatának jóváhagyása</span><span class="sxs-lookup"><span data-stu-id="d7997-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="d7997-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7997-110">EXAMPLES</span></span>

### <span data-ttu-id="d7997-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d7997-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="d7997-112">Ez a parancs jóváhagyja a replikációt a MyAnfVolume-on.</span><span class="sxs-lookup"><span data-stu-id="d7997-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="d7997-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7997-113">PARAMETERS</span></span>

### <span data-ttu-id="d7997-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7997-114">-AccountName</span></span>
<span data-ttu-id="d7997-115">A replikációs forráskötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="d7997-115">The name of the ANF account of the replication source volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7997-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="d7997-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="d7997-117">A céladatvédelmi mennyiség fájlrendszer-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d7997-117">The file system id of the destination data protection volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7997-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7997-118">-DefaultProfile</span></span>
<span data-ttu-id="d7997-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7997-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7997-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7997-120">-InputObject</span></span>
<span data-ttu-id="d7997-121">AnF-forráskötet-objektum a replikációs célhely engedélyének beállításához</span><span class="sxs-lookup"><span data-stu-id="d7997-121">The ANF source volume object to authorized the replication destination</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7997-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d7997-122">-Name</span></span>
<span data-ttu-id="d7997-123">Az ANF-replikációs forráskötet neve</span><span class="sxs-lookup"><span data-stu-id="d7997-123">The name of the ANF replication source volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7997-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7997-124">-PassThru</span></span>
<span data-ttu-id="d7997-125">Annak visszaadása, hogy a megadott kötet replikációs engedélyezése történt-e</span><span class="sxs-lookup"><span data-stu-id="d7997-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="d7997-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d7997-126">-PoolName</span></span>
<span data-ttu-id="d7997-127">A replikációs forráskötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="d7997-127">The name of the ANF pool of the replication source volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7997-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7997-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7997-129">Az ANF replikációs forráskötet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="d7997-129">The resource group of the ANF replication source volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7997-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7997-130">-ResourceId</span></span>
<span data-ttu-id="d7997-131">Az ANF-replikációs forráskötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d7997-131">The resource id of the ANF replication source volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7997-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7997-132">-Confirm</span></span>
<span data-ttu-id="d7997-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d7997-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7997-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7997-134">-WhatIf</span></span>
<span data-ttu-id="d7997-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d7997-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7997-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7997-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7997-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7997-137">CommonParameters</span></span>
<span data-ttu-id="d7997-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7997-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7997-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7997-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7997-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7997-140">INPUTS</span></span>

### <span data-ttu-id="d7997-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d7997-141">System.String</span></span>

### <span data-ttu-id="d7997-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d7997-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d7997-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7997-143">OUTPUTS</span></span>

### <span data-ttu-id="d7997-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7997-144">System.Boolean</span></span>

## <span data-ttu-id="d7997-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7997-145">NOTES</span></span>

## <span data-ttu-id="d7997-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7997-146">RELATED LINKS</span></span>
