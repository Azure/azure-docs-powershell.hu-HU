---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 398cc4b8f23ca5296aec741eb720833f589b0e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494130"
---
# <span data-ttu-id="b00c0-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b00c0-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="b00c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b00c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b00c0-103">Információt AD a tartomány kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="b00c0-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b00c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b00c0-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b00c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b00c0-105">DESCRIPTION</span></span>
<span data-ttu-id="b00c0-106">A **Get-AzureRmVMADDomainExtension** parancsmag információkat kap a megadott Azure Active Directory-tartomány (ad) tartomány-kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="b00c0-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="b00c0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b00c0-107">EXAMPLES</span></span>

## <span data-ttu-id="b00c0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b00c0-108">PARAMETERS</span></span>

### <span data-ttu-id="b00c0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00c0-109">-DefaultProfile</span></span>
<span data-ttu-id="b00c0-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b00c0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b00c0-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b00c0-111">-Name</span></span>
<span data-ttu-id="b00c0-112">A tartomány kiterjesztésének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b00c0-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b00c0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00c0-113">-ResourceGroupName</span></span>
<span data-ttu-id="b00c0-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b00c0-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b00c0-115">-Állapot</span><span class="sxs-lookup"><span data-stu-id="b00c0-115">-Status</span></span>
<span data-ttu-id="b00c0-116">Azt jelzi, hogy ez a parancsmag a tartományi bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b00c0-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b00c0-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="b00c0-117">-VMName</span></span>
<span data-ttu-id="b00c0-118">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b00c0-118">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b00c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00c0-119">CommonParameters</span></span>
<span data-ttu-id="b00c0-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b00c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00c0-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00c0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00c0-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b00c0-122">INPUTS</span></span>

### <span data-ttu-id="b00c0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b00c0-123">System.String</span></span>

### <span data-ttu-id="b00c0-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b00c0-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b00c0-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b00c0-125">OUTPUTS</span></span>

### <span data-ttu-id="b00c0-126">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="b00c0-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="b00c0-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b00c0-127">NOTES</span></span>

## <span data-ttu-id="b00c0-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b00c0-128">RELATED LINKS</span></span>

[<span data-ttu-id="b00c0-129">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b00c0-129">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


