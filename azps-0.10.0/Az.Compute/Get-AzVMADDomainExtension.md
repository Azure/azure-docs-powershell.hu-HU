---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844633"
---
# <span data-ttu-id="27724-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="27724-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="27724-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27724-102">SYNOPSIS</span></span>
<span data-ttu-id="27724-103">Információt AD a tartomány kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="27724-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="27724-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27724-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27724-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27724-105">DESCRIPTION</span></span>
<span data-ttu-id="27724-106">A **Get-AzVMADDomainExtension** parancsmag információkat kap a megadott Azure Active Directory-tartomány (ad) tartomány-kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="27724-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="27724-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27724-107">EXAMPLES</span></span>

### <span data-ttu-id="27724-108">1:</span><span class="sxs-lookup"><span data-stu-id="27724-108">1:</span></span>
```

```

## <span data-ttu-id="27724-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27724-109">PARAMETERS</span></span>

### <span data-ttu-id="27724-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27724-110">-DefaultProfile</span></span>
<span data-ttu-id="27724-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27724-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27724-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27724-112">-Name</span></span>
<span data-ttu-id="27724-113">A tartomány kiterjesztésének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="27724-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="27724-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27724-114">-ResourceGroupName</span></span>
<span data-ttu-id="27724-115">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="27724-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="27724-116">-Állapot</span><span class="sxs-lookup"><span data-stu-id="27724-116">-Status</span></span>
<span data-ttu-id="27724-117">Azt jelzi, hogy ez a parancsmag a tartományi bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="27724-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="27724-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="27724-118">-VMName</span></span>
<span data-ttu-id="27724-119">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="27724-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="27724-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27724-120">CommonParameters</span></span>
<span data-ttu-id="27724-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27724-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27724-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27724-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27724-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27724-123">INPUTS</span></span>

### <span data-ttu-id="27724-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="27724-124">None</span></span>
<span data-ttu-id="27724-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="27724-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27724-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27724-126">OUTPUTS</span></span>

### <span data-ttu-id="27724-127">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="27724-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="27724-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27724-128">NOTES</span></span>

## <span data-ttu-id="27724-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27724-129">RELATED LINKS</span></span>

[<span data-ttu-id="27724-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="27724-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


