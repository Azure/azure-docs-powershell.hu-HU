---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672158"
---
# <span data-ttu-id="8ec91-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="8ec91-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="8ec91-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ec91-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec91-103">A piactér-terv adatait egy virtuális gépen állítja be.</span><span class="sxs-lookup"><span data-stu-id="8ec91-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ec91-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ec91-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ec91-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ec91-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec91-106">A **set-AzureRmVMPlan** parancsmag a virtuális gép Azure Marketplace csomagjának adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="8ec91-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="8ec91-107">Mielőtt a piactéren keresztül telepíteni szeretné a Piactért, a programozott hozzáférést engedélyeznie kell, vagy a virtuális gépet az Azure Portal segítségével kell telepítenie.</span><span class="sxs-lookup"><span data-stu-id="8ec91-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="8ec91-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8ec91-108">EXAMPLES</span></span>

## <span data-ttu-id="8ec91-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ec91-109">PARAMETERS</span></span>

### <span data-ttu-id="8ec91-110">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ec91-110">-Name</span></span>
<span data-ttu-id="8ec91-111">A piactéren a kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec91-111">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="8ec91-112">Ez a Get-AzureRmVMImageSku parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="8ec91-112">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="8ec91-113">A képinformációk megkereséséről további információt az [Azure Virtual Machine-képek, a PowerShell és az Azure CLI használata](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) a Microsoft Azure dokumentációban című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8ec91-113">For more information about how to find image information, see [Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="8ec91-114">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="8ec91-114">-Product</span></span>
<span data-ttu-id="8ec91-115">A piactéren a kép szorzatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec91-115">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="8ec91-116">Ez ugyanaz az információ, mint a **imageReference** elem **ajánlati** értéke.</span><span class="sxs-lookup"><span data-stu-id="8ec91-116">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec91-117">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="8ec91-117">-PromotionCode</span></span>
<span data-ttu-id="8ec91-118">Egy előléptetési kódot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8ec91-118">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec91-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8ec91-119">-Publisher</span></span>
<span data-ttu-id="8ec91-120">A kép közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec91-120">Specifies the publisher of the image.</span></span>
<span data-ttu-id="8ec91-121">Ezeket az információkat az Get-AzureRmVMImagePublisher parancsmag segítségével találja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec91-121">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec91-122">-VM</span><span class="sxs-lookup"><span data-stu-id="8ec91-122">-VM</span></span>
<span data-ttu-id="8ec91-123">Annak a virtuális gépnek az objektumát adja meg, amelyhez a piactér-csomagot be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="8ec91-123">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="8ec91-124">A Virtual Machine-objektum beolvasásához az Get-AzureRmVM parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="8ec91-124">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="8ec91-125">A New-AzureRmVMConfig parancsmag segítségével létrehozhatja a virtuálisgép-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="8ec91-125">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec91-126">CommonParameters</span></span>
<span data-ttu-id="8ec91-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ec91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec91-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec91-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec91-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ec91-129">INPUTS</span></span>

### <span data-ttu-id="8ec91-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="8ec91-130">None</span></span>
<span data-ttu-id="8ec91-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8ec91-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ec91-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ec91-132">OUTPUTS</span></span>

## <span data-ttu-id="8ec91-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ec91-133">NOTES</span></span>

## <span data-ttu-id="8ec91-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ec91-134">RELATED LINKS</span></span>

[<span data-ttu-id="8ec91-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ec91-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8ec91-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8ec91-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="8ec91-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8ec91-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8ec91-138">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="8ec91-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
