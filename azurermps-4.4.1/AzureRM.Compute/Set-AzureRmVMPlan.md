---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: 9fc5da6afd281f68329274ae62a67d888aa13260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505608"
---
# <span data-ttu-id="c6450-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="c6450-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="c6450-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6450-102">SYNOPSIS</span></span>
<span data-ttu-id="c6450-103">A piactér-terv adatait egy virtuális gépen állítja be.</span><span class="sxs-lookup"><span data-stu-id="c6450-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6450-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6450-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6450-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6450-105">DESCRIPTION</span></span>
<span data-ttu-id="c6450-106">A **set-AzureRmVMPlan** parancsmag a virtuális gép Azure Marketplace csomagjának adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="c6450-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="c6450-107">Mielőtt a piactéren keresztül telepíteni szeretné a Piactért, a programozott hozzáférést engedélyeznie kell, vagy a virtuális gépet az Azure Portal segítségével kell telepítenie.</span><span class="sxs-lookup"><span data-stu-id="c6450-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="c6450-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c6450-108">EXAMPLES</span></span>

## <span data-ttu-id="c6450-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6450-109">PARAMETERS</span></span>

### <span data-ttu-id="c6450-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6450-110">-DefaultProfile</span></span>
<span data-ttu-id="c6450-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6450-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6450-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6450-112">-Name</span></span>
<span data-ttu-id="c6450-113">A piactéren a kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6450-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="c6450-114">Ez a Get-AzureRmVMImageSku parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="c6450-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="c6450-115">A képinformációk megkereséséről további információt az Azure Virtual Machine-képek – a PowerShell és az Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) a Microsoft Azure-dokumentáció) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6450-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="c6450-116">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="c6450-116">-Product</span></span>
<span data-ttu-id="c6450-117">A piactéren a kép szorzatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6450-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="c6450-118">Ez ugyanaz az információ, mint a **imageReference** elem **ajánlati** értéke.</span><span class="sxs-lookup"><span data-stu-id="c6450-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="c6450-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="c6450-119">-PromotionCode</span></span>
<span data-ttu-id="c6450-120">Egy előléptetési kódot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c6450-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="c6450-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c6450-121">-Publisher</span></span>
<span data-ttu-id="c6450-122">A kép közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6450-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="c6450-123">Ezeket az információkat az Get-AzureRmVMImagePublisher parancsmag segítségével találja meg.</span><span class="sxs-lookup"><span data-stu-id="c6450-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="c6450-124">-VM</span><span class="sxs-lookup"><span data-stu-id="c6450-124">-VM</span></span>
<span data-ttu-id="c6450-125">Annak a virtuális gépnek az objektumát adja meg, amelyhez a piactér-csomagot be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="c6450-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="c6450-126">A Virtual Machine-objektum beolvasásához az Get-AzureRmVM parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="c6450-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="c6450-127">A New-AzureRmVMConfig parancsmag segítségével létrehozhatja a virtuálisgép-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="c6450-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="c6450-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6450-128">CommonParameters</span></span>
<span data-ttu-id="c6450-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6450-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6450-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6450-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6450-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6450-131">INPUTS</span></span>

## <span data-ttu-id="c6450-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6450-132">OUTPUTS</span></span>

## <span data-ttu-id="c6450-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6450-133">NOTES</span></span>

## <span data-ttu-id="c6450-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6450-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6450-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c6450-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="c6450-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c6450-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c6450-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c6450-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c6450-138">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c6450-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)