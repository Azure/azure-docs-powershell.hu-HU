---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 2ec4ec1898e79fd7f7f35a406f2a99f9dd2da6fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667457"
---
# <span data-ttu-id="7de9d-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7de9d-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="7de9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7de9d-102">SYNOPSIS</span></span>
<span data-ttu-id="7de9d-103">Információt AD a tartomány kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="7de9d-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="7de9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7de9d-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7de9d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7de9d-105">DESCRIPTION</span></span>
<span data-ttu-id="7de9d-106">A **Get-AzVMADDomainExtension** parancsmag információkat kap a megadott Azure Active Directory-tartomány (ad) tartomány-kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="7de9d-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="7de9d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7de9d-107">EXAMPLES</span></span>

## <span data-ttu-id="7de9d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7de9d-108">PARAMETERS</span></span>

### <span data-ttu-id="7de9d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de9d-109">-DefaultProfile</span></span>
<span data-ttu-id="7de9d-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7de9d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7de9d-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7de9d-111">-Name</span></span>
<span data-ttu-id="7de9d-112">A tartomány kiterjesztésének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7de9d-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="7de9d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de9d-113">-ResourceGroupName</span></span>
<span data-ttu-id="7de9d-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7de9d-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7de9d-115">-Állapot</span><span class="sxs-lookup"><span data-stu-id="7de9d-115">-Status</span></span>
<span data-ttu-id="7de9d-116">Azt jelzi, hogy ez a parancsmag a tartományi bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7de9d-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="7de9d-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="7de9d-117">-VMName</span></span>
<span data-ttu-id="7de9d-118">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7de9d-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7de9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de9d-119">CommonParameters</span></span>
<span data-ttu-id="7de9d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7de9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de9d-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7de9d-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de9d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7de9d-122">INPUTS</span></span>

### <span data-ttu-id="7de9d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7de9d-123">System.String</span></span>

### <span data-ttu-id="7de9d-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7de9d-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7de9d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7de9d-125">OUTPUTS</span></span>

### <span data-ttu-id="7de9d-126">Microsoft. Azure. commands. kiszámítás. models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="7de9d-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="7de9d-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7de9d-127">NOTES</span></span>

## <span data-ttu-id="7de9d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7de9d-128">RELATED LINKS</span></span>

[<span data-ttu-id="7de9d-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7de9d-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


