---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503852"
---
# <span data-ttu-id="6e16a-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e16a-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="6e16a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e16a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e16a-103">Beolvassa a VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="6e16a-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e16a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e16a-104">SYNTAX</span></span>

### <span data-ttu-id="6e16a-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e16a-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="6e16a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="6e16a-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## <span data-ttu-id="6e16a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e16a-107">DESCRIPTION</span></span>
<span data-ttu-id="6e16a-108">A **Get-AzureRmVmss** parancsmag a virtuálisgép-készlet (VMSS) modell-és példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="6e16a-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6e16a-109">A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="6e16a-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="6e16a-110">A példány nézet a virtuális gép példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="6e16a-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="6e16a-111">Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.</span><span class="sxs-lookup"><span data-stu-id="6e16a-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="6e16a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="6e16a-112">EXAMPLES</span></span>

### <span data-ttu-id="6e16a-113">Példa 1: VMSS tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="6e16a-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="6e16a-114">Ez a parancs beolvassa a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="6e16a-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="6e16a-115">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modell nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="6e16a-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="6e16a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e16a-116">PARAMETERS</span></span>

### <span data-ttu-id="6e16a-117">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="6e16a-117">-InstanceView</span></span>
<span data-ttu-id="6e16a-118">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6e16a-118">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e16a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e16a-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e16a-120">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e16a-120">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e16a-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6e16a-121">-VMScaleSetName</span></span>
<span data-ttu-id="6e16a-122">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="6e16a-122">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e16a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e16a-123">CommonParameters</span></span>
<span data-ttu-id="6e16a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e16a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e16a-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e16a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e16a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e16a-126">INPUTS</span></span>

### <span data-ttu-id="6e16a-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="6e16a-127">None</span></span>
<span data-ttu-id="6e16a-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6e16a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e16a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e16a-129">OUTPUTS</span></span>

### <span data-ttu-id="6e16a-130">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6e16a-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6e16a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e16a-131">NOTES</span></span>

## <span data-ttu-id="6e16a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e16a-132">RELATED LINKS</span></span>

[<span data-ttu-id="6e16a-133">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e16a-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="6e16a-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e16a-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="6e16a-135">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e16a-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="6e16a-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e16a-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="6e16a-137">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e16a-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="6e16a-138">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e16a-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="6e16a-139">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6e16a-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


