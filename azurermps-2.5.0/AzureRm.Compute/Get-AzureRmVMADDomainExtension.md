---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 01a5a69053cfd05186abae45d5b53fff0b022b98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848901"
---
# <span data-ttu-id="e78ca-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="e78ca-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="e78ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e78ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e78ca-103">Információt AD a tartomány kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="e78ca-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e78ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e78ca-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e78ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e78ca-105">DESCRIPTION</span></span>
<span data-ttu-id="e78ca-106">A **Get-AzureRmVMADDomainExtension** parancsmag információkat kap a megadott Azure Active Directory-tartomány (ad) tartomány-kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="e78ca-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="e78ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e78ca-107">EXAMPLES</span></span>

### <span data-ttu-id="e78ca-108">1:</span><span class="sxs-lookup"><span data-stu-id="e78ca-108">1:</span></span>
```

```

## <span data-ttu-id="e78ca-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e78ca-109">PARAMETERS</span></span>

### <span data-ttu-id="e78ca-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e78ca-110">-DefaultProfile</span></span>
<span data-ttu-id="e78ca-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e78ca-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e78ca-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e78ca-112">-Name</span></span>
<span data-ttu-id="e78ca-113">A tartomány kiterjesztésének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e78ca-113">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e78ca-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e78ca-114">-ResourceGroupName</span></span>
<span data-ttu-id="e78ca-115">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e78ca-115">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e78ca-116">-Állapot</span><span class="sxs-lookup"><span data-stu-id="e78ca-116">-Status</span></span>
<span data-ttu-id="e78ca-117">Azt jelzi, hogy ez a parancsmag a tartományi bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e78ca-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e78ca-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="e78ca-118">-VMName</span></span>
<span data-ttu-id="e78ca-119">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e78ca-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e78ca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e78ca-120">CommonParameters</span></span>
<span data-ttu-id="e78ca-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e78ca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e78ca-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e78ca-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e78ca-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e78ca-123">INPUTS</span></span>

### <span data-ttu-id="e78ca-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="e78ca-124">None</span></span>
<span data-ttu-id="e78ca-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e78ca-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e78ca-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e78ca-126">OUTPUTS</span></span>

### <span data-ttu-id="e78ca-127">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="e78ca-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="e78ca-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e78ca-128">NOTES</span></span>

## <span data-ttu-id="e78ca-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e78ca-129">RELATED LINKS</span></span>

[<span data-ttu-id="e78ca-130">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="e78ca-130">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


