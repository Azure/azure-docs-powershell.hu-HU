---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 75b8190c34d5335904d40d386cabc76e8cbf0b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492334"
---
# <span data-ttu-id="8b0e5-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="8b0e5-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="8b0e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0e5-103">Elindítja a VMSS példány manuális frissítését.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b0e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b0e5-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b0e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b0e5-105">DESCRIPTION</span></span>
<span data-ttu-id="8b0e5-106">Az Update-AzureRmVmssInstance parancsmag a megadott virtuálisgép-készlet (VMSS-példány) kézi frissítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="8b0e5-107">Ezt a beállítást akkor használja a rendszer, ha a VMSS-méretarány beállítása beállítás manuális értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="8b0e5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8b0e5-108">EXAMPLES</span></span>

### <span data-ttu-id="8b0e5-109">Példa 1: a VMSS példány frissítésének megkezdése</span><span class="sxs-lookup"><span data-stu-id="8b0e5-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="8b0e5-110">Ez a parancs elindítja a VMScaleSet001 nevű VMSS frissítését, amelynek a példány azonosítója 0.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="8b0e5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b0e5-111">PARAMETERS</span></span>

### <span data-ttu-id="8b0e5-112">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8b0e5-112">-InstanceId</span></span>
<span data-ttu-id="8b0e5-113">Karakterláncként adja meg a frissítendő példány AZONOSÍTÓját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-113">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0e5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0e5-114">-ResourceGroupName</span></span>
<span data-ttu-id="8b0e5-115">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-115">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0e5-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8b0e5-116">-VMScaleSetName</span></span>
<span data-ttu-id="8b0e5-117">Annak a VMSS-példánynak a nevét adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-117">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0e5-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b0e5-118">-Confirm</span></span>
<span data-ttu-id="8b0e5-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0e5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0e5-120">-WhatIf</span></span>
<span data-ttu-id="8b0e5-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8b0e5-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0e5-123">CommonParameters</span></span>
<span data-ttu-id="8b0e5-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b0e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0e5-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0e5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0e5-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b0e5-126">INPUTS</span></span>

### <span data-ttu-id="8b0e5-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="8b0e5-127">None</span></span>
<span data-ttu-id="8b0e5-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b0e5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b0e5-129">OUTPUTS</span></span>

###  
<span data-ttu-id="8b0e5-130">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8b0e5-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8b0e5-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b0e5-131">NOTES</span></span>

## <span data-ttu-id="8b0e5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b0e5-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b0e5-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b0e5-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


