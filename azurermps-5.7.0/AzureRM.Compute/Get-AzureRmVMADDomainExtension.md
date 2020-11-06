---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497727"
---
# <span data-ttu-id="a1291-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a1291-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="a1291-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1291-102">SYNOPSIS</span></span>
<span data-ttu-id="a1291-103">Információt AD a tartomány kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="a1291-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1291-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1291-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="a1291-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1291-105">DESCRIPTION</span></span>
<span data-ttu-id="a1291-106">A **Get-AzureRmVMADDomainExtension** parancsmag információkat kap a megadott Azure Active Directory-tartomány (ad) tartomány-kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="a1291-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="a1291-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a1291-107">EXAMPLES</span></span>

## <span data-ttu-id="a1291-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1291-108">PARAMETERS</span></span>

### <span data-ttu-id="a1291-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1291-109">-Name</span></span>
<span data-ttu-id="a1291-110">A tartomány kiterjesztésének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1291-110">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="a1291-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1291-111">-ResourceGroupName</span></span>
<span data-ttu-id="a1291-112">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1291-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a1291-113">-Állapot</span><span class="sxs-lookup"><span data-stu-id="a1291-113">-Status</span></span>
<span data-ttu-id="a1291-114">Azt jelzi, hogy ez a parancsmag a tartományi bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a1291-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="a1291-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="a1291-115">-VMName</span></span>
<span data-ttu-id="a1291-116">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1291-116">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="a1291-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1291-117">CommonParameters</span></span>
<span data-ttu-id="a1291-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1291-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1291-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1291-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1291-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1291-120">INPUTS</span></span>

### <span data-ttu-id="a1291-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="a1291-121">None</span></span>
<span data-ttu-id="a1291-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a1291-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1291-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1291-123">OUTPUTS</span></span>

## <span data-ttu-id="a1291-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1291-124">NOTES</span></span>

## <span data-ttu-id="a1291-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1291-125">RELATED LINKS</span></span>

[<span data-ttu-id="a1291-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a1291-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


