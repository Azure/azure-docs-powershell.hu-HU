---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850902"
---
# <span data-ttu-id="9ff7a-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="9ff7a-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="9ff7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ff7a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff7a-103">A piactér-terv adatait egy virtuális gépen állítja be.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ff7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ff7a-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ff7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ff7a-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff7a-106">A **set-AzureRmVMPlan** parancsmag a virtuális gép Azure Marketplace csomagjának adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="9ff7a-107">Mielőtt a piactéren keresztül telepíteni szeretné a Piactért, a programozott hozzáférést engedélyeznie kell, vagy a virtuális gépet az Azure Portal segítségével kell telepítenie.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="9ff7a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9ff7a-108">EXAMPLES</span></span>

## <span data-ttu-id="9ff7a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ff7a-109">PARAMETERS</span></span>

### <span data-ttu-id="9ff7a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff7a-110">-DefaultProfile</span></span>
<span data-ttu-id="9ff7a-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ff7a-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ff7a-112">-Name</span></span>
<span data-ttu-id="9ff7a-113">A piactéren a kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="9ff7a-114">Ez a Get-AzureRmVMImageSku parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="9ff7a-115">A képinformációk megkereséséről további információt az Azure Virtual Machine-képek – a PowerShell és az Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) a Microsoft Azure-dokumentáció) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="9ff7a-116">-Szorzat</span><span class="sxs-lookup"><span data-stu-id="9ff7a-116">-Product</span></span>
<span data-ttu-id="9ff7a-117">A piactéren a kép szorzatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="9ff7a-118">Ez ugyanaz az információ, mint a **imageReference** elem **ajánlati** értéke.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="9ff7a-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="9ff7a-119">-PromotionCode</span></span>
<span data-ttu-id="9ff7a-120">Egy előléptetési kódot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="9ff7a-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9ff7a-121">-Publisher</span></span>
<span data-ttu-id="9ff7a-122">A kép közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="9ff7a-123">Ezeket az információkat az Get-AzureRmVMImagePublisher parancsmag segítségével találja meg.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9ff7a-124">-VM</span><span class="sxs-lookup"><span data-stu-id="9ff7a-124">-VM</span></span>
<span data-ttu-id="9ff7a-125">Annak a virtuális gépnek az objektumát adja meg, amelyhez a piactér-csomagot be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="9ff7a-126">A Virtual Machine-objektum beolvasásához az Get-AzureRmVM parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="9ff7a-127">A New-AzureRmVMConfig parancsmag segítségével létrehozhatja a virtuálisgép-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="9ff7a-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="9ff7a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff7a-128">CommonParameters</span></span>
<span data-ttu-id="9ff7a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ff7a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff7a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff7a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff7a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ff7a-131">INPUTS</span></span>

### <span data-ttu-id="9ff7a-132">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9ff7a-132">PSVirtualMachine</span></span>
<span data-ttu-id="9ff7a-133">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9ff7a-133">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9ff7a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ff7a-134">OUTPUTS</span></span>

### <span data-ttu-id="9ff7a-135">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9ff7a-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9ff7a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ff7a-136">NOTES</span></span>

## <span data-ttu-id="9ff7a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ff7a-137">RELATED LINKS</span></span>

[<span data-ttu-id="9ff7a-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9ff7a-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9ff7a-139">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9ff7a-139">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="9ff7a-140">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9ff7a-140">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="9ff7a-141">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9ff7a-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
