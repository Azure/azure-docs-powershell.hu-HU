---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 2b3cf6588f32fd958073ced8d3347733416037ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926705"
---
# <span data-ttu-id="934e3-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="934e3-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="934e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="934e3-102">SYNOPSIS</span></span>
<span data-ttu-id="934e3-103">Azure NetApp-fájlok (ANF)-kötet készletének módosítása</span><span class="sxs-lookup"><span data-stu-id="934e3-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="934e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="934e3-104">SYNTAX</span></span>

### <span data-ttu-id="934e3-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="934e3-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="934e3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="934e3-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="934e3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="934e3-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="934e3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="934e3-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="934e3-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="934e3-109">DESCRIPTION</span></span>
<span data-ttu-id="934e3-110">A **Set-AzNetAppFilesVolumePool** parancsmag módosítja az ANF-kötetek készletét.</span><span class="sxs-lookup"><span data-stu-id="934e3-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="934e3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="934e3-111">EXAMPLES</span></span>

### <span data-ttu-id="934e3-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="934e3-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="934e3-113">Ez módosítja a MyVolume kötet készletét a 7d6e4069-6c78-6c61-7bf6-c60968e45fbf azonosítóval</span><span class="sxs-lookup"><span data-stu-id="934e3-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="934e3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="934e3-114">PARAMETERS</span></span>

### <span data-ttu-id="934e3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="934e3-115">-AccountName</span></span>
<span data-ttu-id="934e3-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="934e3-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="934e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="934e3-117">-DefaultProfile</span></span>
<span data-ttu-id="934e3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="934e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="934e3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="934e3-119">-InputObject</span></span>
<span data-ttu-id="934e3-120">Az áthelyezni megfelelő hangerő-objektum</span><span class="sxs-lookup"><span data-stu-id="934e3-120">The volume object to move</span></span>

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

### <span data-ttu-id="934e3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="934e3-121">-Name</span></span>
<span data-ttu-id="934e3-122">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="934e3-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="934e3-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="934e3-123">-NewPoolResourceId</span></span>
<span data-ttu-id="934e3-124">Annak a kapacitáskészletnek az Erőforrásazonosítója, amelybe át kell lépni.</span><span class="sxs-lookup"><span data-stu-id="934e3-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="934e3-125">A készlet azonosítására használt UUID v4</span><span class="sxs-lookup"><span data-stu-id="934e3-125">UUID v4 used to identify the pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="934e3-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="934e3-126">-PoolName</span></span>
<span data-ttu-id="934e3-127">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="934e3-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="934e3-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="934e3-128">-PoolObject</span></span>
<span data-ttu-id="934e3-129">A hangerőt tartalmazó készletobjektum</span><span class="sxs-lookup"><span data-stu-id="934e3-129">The pool object containing the volume</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="934e3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="934e3-130">-ResourceGroupName</span></span>
<span data-ttu-id="934e3-131">Az ANF-mennyiség erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="934e3-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="934e3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="934e3-132">-ResourceId</span></span>
<span data-ttu-id="934e3-133">Az ANF-mennyiség erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="934e3-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="934e3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="934e3-134">-Confirm</span></span>
<span data-ttu-id="934e3-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="934e3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="934e3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="934e3-136">-WhatIf</span></span>
<span data-ttu-id="934e3-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="934e3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="934e3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="934e3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="934e3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="934e3-139">CommonParameters</span></span>
<span data-ttu-id="934e3-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="934e3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="934e3-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="934e3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="934e3-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="934e3-142">INPUTS</span></span>

### <span data-ttu-id="934e3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="934e3-143">System.String</span></span>

### <span data-ttu-id="934e3-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="934e3-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="934e3-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="934e3-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="934e3-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="934e3-146">OUTPUTS</span></span>

### <span data-ttu-id="934e3-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="934e3-147">System.Boolean</span></span>

## <span data-ttu-id="934e3-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="934e3-148">NOTES</span></span>

## <span data-ttu-id="934e3-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="934e3-149">RELATED LINKS</span></span>
