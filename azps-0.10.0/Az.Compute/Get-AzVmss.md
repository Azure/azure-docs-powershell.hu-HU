---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844553"
---
# <span data-ttu-id="170ac-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="170ac-101">Get-AzVmss</span></span>

## <span data-ttu-id="170ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="170ac-102">SYNOPSIS</span></span>
<span data-ttu-id="170ac-103">Beolvassa a VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="170ac-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="170ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="170ac-104">SYNTAX</span></span>

### <span data-ttu-id="170ac-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="170ac-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="170ac-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="170ac-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="170ac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="170ac-107">DESCRIPTION</span></span>
<span data-ttu-id="170ac-108">A **Get-AzVmss** parancsmag a virtuálisgép-készlet (VMSS) modell-és példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="170ac-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="170ac-109">A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="170ac-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="170ac-110">A példány nézet a virtuális gép példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="170ac-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="170ac-111">Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.</span><span class="sxs-lookup"><span data-stu-id="170ac-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="170ac-112">Példák</span><span class="sxs-lookup"><span data-stu-id="170ac-112">EXAMPLES</span></span>

### <span data-ttu-id="170ac-113">Példa 1: VMSS tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="170ac-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="170ac-114">Ez a parancs beolvassa a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="170ac-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="170ac-115">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modell nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="170ac-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="170ac-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="170ac-116">PARAMETERS</span></span>

### <span data-ttu-id="170ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170ac-117">-DefaultProfile</span></span>
<span data-ttu-id="170ac-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="170ac-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170ac-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="170ac-119">-InstanceView</span></span>
<span data-ttu-id="170ac-120">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="170ac-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="170ac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170ac-121">-ResourceGroupName</span></span>
<span data-ttu-id="170ac-122">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="170ac-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="170ac-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="170ac-123">-VMScaleSetName</span></span>
<span data-ttu-id="170ac-124">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="170ac-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="170ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170ac-125">CommonParameters</span></span>
<span data-ttu-id="170ac-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="170ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170ac-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170ac-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170ac-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="170ac-128">INPUTS</span></span>

### <span data-ttu-id="170ac-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="170ac-129">None</span></span>
<span data-ttu-id="170ac-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="170ac-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="170ac-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="170ac-131">OUTPUTS</span></span>

### <span data-ttu-id="170ac-132">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="170ac-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="170ac-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="170ac-133">NOTES</span></span>

## <span data-ttu-id="170ac-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="170ac-134">RELATED LINKS</span></span>

[<span data-ttu-id="170ac-135">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="170ac-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="170ac-136">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="170ac-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="170ac-137">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="170ac-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="170ac-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="170ac-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="170ac-139">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="170ac-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="170ac-140">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="170ac-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="170ac-141">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="170ac-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


