---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 16eb962245502338c7b12f6e5abf20a9bc04b83f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837706"
---
# <span data-ttu-id="3b0f0-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="3b0f0-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="3b0f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0f0-103">Azure NetApp-fájlok (ANF) pillanatképének törlése.</span><span class="sxs-lookup"><span data-stu-id="3b0f0-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="3b0f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b0f0-104">SYNTAX</span></span>

### <span data-ttu-id="3b0f0-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b0f0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b0f0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b0f0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b0f0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b0f0-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b0f0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b0f0-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b0f0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b0f0-109">DESCRIPTION</span></span>
<span data-ttu-id="3b0f0-110">A **Remove-AzNetAppFilesSnapshot** parancsmag törli a ANF-pillanatfelvételt.</span><span class="sxs-lookup"><span data-stu-id="3b0f0-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="3b0f0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3b0f0-111">EXAMPLES</span></span>

### <span data-ttu-id="3b0f0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b0f0-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="3b0f0-113">Ez a parancs törli a "MyAnfSnapshot" ANF-pillanatfelvételt.</span><span class="sxs-lookup"><span data-stu-id="3b0f0-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="3b0f0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b0f0-114">PARAMETERS</span></span>

### <span data-ttu-id="3b0f0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b0f0-115">-AccountName</span></span>
<span data-ttu-id="3b0f0-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="3b0f0-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0f0-117">-DefaultProfile</span></span>
<span data-ttu-id="3b0f0-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b0f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b0f0-119">-InputObject</span></span>
<span data-ttu-id="3b0f0-120">Az eltávolítandó pillanatkép-objektum</span><span class="sxs-lookup"><span data-stu-id="3b0f0-120">The snapshot object to remove</span></span>

```yaml
Type: PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b0f0-121">-Name</span></span>
<span data-ttu-id="3b0f0-122">A ANF pillanatképének neve</span><span class="sxs-lookup"><span data-stu-id="3b0f0-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b0f0-123">-PassThru</span></span>
<span data-ttu-id="3b0f0-124">A megadott kötet sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="3b0f0-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="3b0f0-125">-PoolName</span></span>
<span data-ttu-id="3b0f0-126">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="3b0f0-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b0f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="3b0f0-128">A ANF pillanatképének erőforráscsoport csoportja</span><span class="sxs-lookup"><span data-stu-id="3b0f0-128">The resource group of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b0f0-129">-ResourceId</span></span>
<span data-ttu-id="3b0f0-130">A ANF pillanatképének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3b0f0-130">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-131">-Kötetnév</span><span class="sxs-lookup"><span data-stu-id="3b0f0-131">-VolumeName</span></span>
<span data-ttu-id="3b0f0-132">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="3b0f0-132">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="3b0f0-133">-VolumeObject</span></span>
<span data-ttu-id="3b0f0-134">Az eltávolítandó pillanatképet tartalmazó kötet objektum</span><span class="sxs-lookup"><span data-stu-id="3b0f0-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b0f0-135">-Confirm</span></span>
<span data-ttu-id="3b0f0-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b0f0-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b0f0-137">-WhatIf</span></span>
<span data-ttu-id="3b0f0-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b0f0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b0f0-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b0f0-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0f0-140">CommonParameters</span></span>
<span data-ttu-id="3b0f0-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b0f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3b0f0-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b0f0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0f0-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b0f0-143">INPUTS</span></span>

### <span data-ttu-id="3b0f0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3b0f0-144">System.String</span></span>

### <span data-ttu-id="3b0f0-145">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3b0f0-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="3b0f0-146">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="3b0f0-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="3b0f0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b0f0-147">OUTPUTS</span></span>

### <span data-ttu-id="3b0f0-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b0f0-148">System.Boolean</span></span>

## <span data-ttu-id="3b0f0-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b0f0-149">NOTES</span></span>

## <span data-ttu-id="3b0f0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b0f0-150">RELATED LINKS</span></span>
