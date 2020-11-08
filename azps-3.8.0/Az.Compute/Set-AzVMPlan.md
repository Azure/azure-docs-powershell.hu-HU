---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014623"
---
# <span data-ttu-id="75d31-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="75d31-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="75d31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75d31-102">SYNOPSIS</span></span>
<span data-ttu-id="75d31-103">A piactér-terv adatait egy virtuális gépen állítja be.</span><span class="sxs-lookup"><span data-stu-id="75d31-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="75d31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75d31-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="75d31-105">DESCRIPTION</span></span>
<span data-ttu-id="75d31-106">A **set-AzVMPlan** parancsmag a virtuális gép Azure Marketplace csomagjának adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="75d31-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="75d31-107">Mielőtt a piactéren keresztül telepíteni szeretné a Piactért, a programozott hozzáférést engedélyeznie kell, vagy a virtuális gépet az Azure Portal segítségével kell telepítenie.</span><span class="sxs-lookup"><span data-stu-id="75d31-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="75d31-108">Példák</span><span class="sxs-lookup"><span data-stu-id="75d31-108">EXAMPLES</span></span>

## <span data-ttu-id="75d31-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75d31-109">PARAMETERS</span></span>

### <span data-ttu-id="75d31-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d31-110">-DefaultProfile</span></span>
<span data-ttu-id="75d31-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75d31-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75d31-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75d31-112">-Name</span></span>
<span data-ttu-id="75d31-113">A piactéren a kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75d31-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="75d31-114">Ez a Get-AzVMImageSku parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="75d31-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="75d31-115">A képinformációk megkereséséről további információt az Azure Virtual Machine-képek – a PowerShell és az Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) a Microsoft Azure-dokumentáció) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="75d31-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="75d31-116">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="75d31-116">-Product</span></span>
<span data-ttu-id="75d31-117">A piactéren a kép szorzatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="75d31-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="75d31-118">Ez ugyanaz az információ, mint a **imageReference** elem **ajánlati** értéke.</span><span class="sxs-lookup"><span data-stu-id="75d31-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="75d31-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="75d31-119">-PromotionCode</span></span>
<span data-ttu-id="75d31-120">Egy előléptetési kódot ad meg.</span><span class="sxs-lookup"><span data-stu-id="75d31-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="75d31-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="75d31-121">-Publisher</span></span>
<span data-ttu-id="75d31-122">A kép közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75d31-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="75d31-123">Ezeket az információkat az Get-AzVMImagePublisher parancsmag segítségével találja meg.</span><span class="sxs-lookup"><span data-stu-id="75d31-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="75d31-124">-VM</span><span class="sxs-lookup"><span data-stu-id="75d31-124">-VM</span></span>
<span data-ttu-id="75d31-125">Annak a virtuális gépnek az objektumát adja meg, amelyhez a piactér-csomagot be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="75d31-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="75d31-126">A Virtual Machine-objektum beolvasásához az Get-AzVM parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="75d31-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="75d31-127">A New-AzVMConfig parancsmag segítségével létrehozhatja a virtuálisgép-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="75d31-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="75d31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d31-128">CommonParameters</span></span>
<span data-ttu-id="75d31-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75d31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d31-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="75d31-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d31-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75d31-131">INPUTS</span></span>

### <span data-ttu-id="75d31-132">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="75d31-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="75d31-133">System. String</span><span class="sxs-lookup"><span data-stu-id="75d31-133">System.String</span></span>

## <span data-ttu-id="75d31-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75d31-134">OUTPUTS</span></span>

### <span data-ttu-id="75d31-135">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="75d31-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="75d31-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75d31-136">NOTES</span></span>

## <span data-ttu-id="75d31-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75d31-137">RELATED LINKS</span></span>

[<span data-ttu-id="75d31-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="75d31-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="75d31-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="75d31-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="75d31-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="75d31-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="75d31-141">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="75d31-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
