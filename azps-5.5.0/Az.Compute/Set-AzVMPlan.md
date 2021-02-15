---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164202"
---
# <span data-ttu-id="63a8c-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="63a8c-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="63a8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="63a8c-103">Beállítja a Piactér-terv adatait egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="63a8c-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="63a8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63a8c-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63a8c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="63a8c-106">A **Set-AzVMPlan** parancsmag beállítja az Azure Piactér tervének adatait egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="63a8c-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="63a8c-107">Mielőtt üzembe helyezhetne egy Piactér-képet a parancssoron keresztül, engedélyeznie kell a programozott hozzáférést, vagy a virtuális gépet az Azure Portal használatával kell üzembe helyeznie.</span><span class="sxs-lookup"><span data-stu-id="63a8c-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="63a8c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63a8c-108">EXAMPLES</span></span>

## <span data-ttu-id="63a8c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63a8c-109">PARAMETERS</span></span>

### <span data-ttu-id="63a8c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a8c-110">-DefaultProfile</span></span>
<span data-ttu-id="63a8c-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63a8c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63a8c-112">-Name</span><span class="sxs-lookup"><span data-stu-id="63a8c-112">-Name</span></span>
<span data-ttu-id="63a8c-113">A kép nevét adja meg a Piactérről.</span><span class="sxs-lookup"><span data-stu-id="63a8c-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="63a8c-114">Ez a parancsmag által visszaadott Get-AzVMImageSku érték.</span><span class="sxs-lookup"><span data-stu-id="63a8c-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="63a8c-115">A képinformációk keresésével kapcsolatos további információkért lásd a Navigálás és az Azure Virtuálisgép-képek kiválasztása a PowerShell és az Azure CLI segítségével https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (a https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) Microsoft Azure dokumentációjában).</span><span class="sxs-lookup"><span data-stu-id="63a8c-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a8c-116">-Product</span><span class="sxs-lookup"><span data-stu-id="63a8c-116">-Product</span></span>
<span data-ttu-id="63a8c-117">A kép termékét adja meg a Piactérről.</span><span class="sxs-lookup"><span data-stu-id="63a8c-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="63a8c-118">Ezek ugyanazok az információk, mint a **képReferencia** elem Ajánlat értéke. </span><span class="sxs-lookup"><span data-stu-id="63a8c-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a8c-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="63a8c-119">-PromotionCode</span></span>
<span data-ttu-id="63a8c-120">Megadja a promóciós kódot.</span><span class="sxs-lookup"><span data-stu-id="63a8c-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a8c-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="63a8c-121">-Publisher</span></span>
<span data-ttu-id="63a8c-122">A kép közzétevője.</span><span class="sxs-lookup"><span data-stu-id="63a8c-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="63a8c-123">Ezek az információk a Get-AzVMImagePublisher segítségével találják meg.</span><span class="sxs-lookup"><span data-stu-id="63a8c-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a8c-124">-VM</span><span class="sxs-lookup"><span data-stu-id="63a8c-124">-VM</span></span>
<span data-ttu-id="63a8c-125">Azt a virtuális gépobjektumot adja meg, amelyhez piactér-tervet kell beállítani.</span><span class="sxs-lookup"><span data-stu-id="63a8c-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="63a8c-126">A Get-AzVM használhatja virtuális gépi objektum beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="63a8c-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="63a8c-127">A New-AzVMConfig virtuális gépi objektum létrehozásához használhatja.</span><span class="sxs-lookup"><span data-stu-id="63a8c-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63a8c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a8c-128">CommonParameters</span></span>
<span data-ttu-id="63a8c-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a8c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a8c-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63a8c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a8c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63a8c-131">INPUTS</span></span>

### <span data-ttu-id="63a8c-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="63a8c-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="63a8c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="63a8c-133">System.String</span></span>

## <span data-ttu-id="63a8c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63a8c-134">OUTPUTS</span></span>

### <span data-ttu-id="63a8c-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="63a8c-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="63a8c-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63a8c-136">NOTES</span></span>

## <span data-ttu-id="63a8c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63a8c-137">RELATED LINKS</span></span>

[<span data-ttu-id="63a8c-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="63a8c-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="63a8c-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="63a8c-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="63a8c-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="63a8c-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="63a8c-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="63a8c-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
