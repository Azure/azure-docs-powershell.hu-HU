---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372734"
---
# <span data-ttu-id="dbd24-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="dbd24-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="dbd24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd24-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd24-103">Azure NetApp-fájlok (ANF)-kötet készletének módosítása</span><span class="sxs-lookup"><span data-stu-id="dbd24-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="dbd24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dbd24-104">SYNTAX</span></span>

### <span data-ttu-id="dbd24-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dbd24-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbd24-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbd24-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbd24-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbd24-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbd24-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbd24-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbd24-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dbd24-109">DESCRIPTION</span></span>
<span data-ttu-id="dbd24-110">A **Set-AzNetAppFilesVolumePool** parancsmag módosítja az ANF-kötetek készletét.</span><span class="sxs-lookup"><span data-stu-id="dbd24-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="dbd24-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dbd24-111">EXAMPLES</span></span>

### <span data-ttu-id="dbd24-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="dbd24-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="dbd24-113">Ez módosítja a MyVolume kötet készletét a 7d6e4069-6c78-6c61-7bf6-c60968e45fbf azonosítóval</span><span class="sxs-lookup"><span data-stu-id="dbd24-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="dbd24-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbd24-114">PARAMETERS</span></span>

### <span data-ttu-id="dbd24-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dbd24-115">-AccountName</span></span>
<span data-ttu-id="dbd24-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="dbd24-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="dbd24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd24-117">-DefaultProfile</span></span>
<span data-ttu-id="dbd24-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbd24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd24-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbd24-119">-InputObject</span></span>
<span data-ttu-id="dbd24-120">Az áthelyezni megfelelő hangerő-objektum</span><span class="sxs-lookup"><span data-stu-id="dbd24-120">The volume object to move</span></span>

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

### <span data-ttu-id="dbd24-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dbd24-121">-Name</span></span>
<span data-ttu-id="dbd24-122">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="dbd24-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="dbd24-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="dbd24-123">-NewPoolResourceId</span></span>
<span data-ttu-id="dbd24-124">Annak a kapacitáskészletnek az Erőforrásazonosítója, amelybe át kell lépni.</span><span class="sxs-lookup"><span data-stu-id="dbd24-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="dbd24-125">A készlet azonosítására használt UUID v4</span><span class="sxs-lookup"><span data-stu-id="dbd24-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="dbd24-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="dbd24-126">-PoolName</span></span>
<span data-ttu-id="dbd24-127">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="dbd24-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="dbd24-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="dbd24-128">-PoolObject</span></span>
<span data-ttu-id="dbd24-129">A hangerőt tartalmazó készletobjektum</span><span class="sxs-lookup"><span data-stu-id="dbd24-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="dbd24-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd24-130">-ResourceGroupName</span></span>
<span data-ttu-id="dbd24-131">Az ANF-mennyiség erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="dbd24-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="dbd24-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbd24-132">-ResourceId</span></span>
<span data-ttu-id="dbd24-133">Az ANF-mennyiség erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="dbd24-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="dbd24-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbd24-134">-Confirm</span></span>
<span data-ttu-id="dbd24-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dbd24-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd24-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbd24-136">-WhatIf</span></span>
<span data-ttu-id="dbd24-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dbd24-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbd24-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dbd24-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd24-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd24-139">CommonParameters</span></span>
<span data-ttu-id="dbd24-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd24-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd24-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbd24-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd24-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbd24-142">INPUTS</span></span>

### <span data-ttu-id="dbd24-143">System.String</span><span class="sxs-lookup"><span data-stu-id="dbd24-143">System.String</span></span>

### <span data-ttu-id="dbd24-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="dbd24-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="dbd24-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="dbd24-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="dbd24-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbd24-146">OUTPUTS</span></span>

### <span data-ttu-id="dbd24-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dbd24-147">System.Boolean</span></span>

## <span data-ttu-id="dbd24-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dbd24-148">NOTES</span></span>

## <span data-ttu-id="dbd24-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbd24-149">RELATED LINKS</span></span>
