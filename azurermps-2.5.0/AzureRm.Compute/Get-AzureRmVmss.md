---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
ms.openlocfilehash: ec66d20e0d9a63b8101b1a9a46410c9e64ac2079
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849777"
---
# <span data-ttu-id="d5902-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d5902-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="d5902-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5902-102">SYNOPSIS</span></span>
<span data-ttu-id="d5902-103">Beolvassa a VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d5902-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5902-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5902-104">SYNTAX</span></span>

### <span data-ttu-id="d5902-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5902-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5902-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d5902-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5902-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5902-107">DESCRIPTION</span></span>
<span data-ttu-id="d5902-108">A **Get-AzureRmVmss** parancsmag a virtuálisgép-készlet (VMSS) modell-és példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="d5902-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d5902-109">A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="d5902-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="d5902-110">A példány nézet a virtuális gép példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="d5902-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="d5902-111">Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.</span><span class="sxs-lookup"><span data-stu-id="d5902-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="d5902-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d5902-112">EXAMPLES</span></span>

### <span data-ttu-id="d5902-113">Példa 1: VMSS tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="d5902-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="d5902-114">Ez a parancs beolvassa a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d5902-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="d5902-115">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modell nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="d5902-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="d5902-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5902-116">PARAMETERS</span></span>

### <span data-ttu-id="d5902-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5902-117">-DefaultProfile</span></span>
<span data-ttu-id="d5902-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5902-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5902-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="d5902-119">-InstanceView</span></span>
<span data-ttu-id="d5902-120">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5902-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5902-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5902-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5902-122">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5902-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="d5902-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d5902-123">-VMScaleSetName</span></span>
<span data-ttu-id="d5902-124">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="d5902-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="d5902-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5902-125">CommonParameters</span></span>
<span data-ttu-id="d5902-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5902-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5902-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5902-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5902-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5902-128">INPUTS</span></span>

### <span data-ttu-id="d5902-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="d5902-129">None</span></span>
<span data-ttu-id="d5902-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d5902-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d5902-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5902-131">OUTPUTS</span></span>

### <span data-ttu-id="d5902-132">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d5902-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d5902-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5902-133">NOTES</span></span>

## <span data-ttu-id="d5902-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5902-134">RELATED LINKS</span></span>

[<span data-ttu-id="d5902-135">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d5902-135">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="d5902-136">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d5902-136">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="d5902-137">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d5902-137">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="d5902-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d5902-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="d5902-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d5902-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="d5902-140">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d5902-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="d5902-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d5902-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


