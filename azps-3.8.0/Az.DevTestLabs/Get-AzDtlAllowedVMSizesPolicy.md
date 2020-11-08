---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012364"
---
# <span data-ttu-id="ff9c6-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ff9c6-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="ff9c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9c6-103">Beilleszti az engedélyezett virtuálisgép-méretekre vonatkozó házirendet a DevTest Labs szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="ff9c6-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="ff9c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff9c6-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff9c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ff9c6-106">A **Get-AzDtlAllowedVMSizesPolicy** parancsmag az engedélyezett virtuálisgép-méretekre vonatkozó házirendet kapja meg, amely lehetővé teszi, hogy megadhatja a laboratóriumban engedélyezett virtuális gépek méretének listáját.</span><span class="sxs-lookup"><span data-stu-id="ff9c6-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="ff9c6-107">A parancsmag az engedélyezett vagy letiltott állapotot adja meg a házirendnek, valamint a megadott házirendben beállított összes virtuális számítógép méretének listáját.</span><span class="sxs-lookup"><span data-stu-id="ff9c6-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="ff9c6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ff9c6-108">EXAMPLES</span></span>

## <span data-ttu-id="ff9c6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff9c6-109">PARAMETERS</span></span>

### <span data-ttu-id="ff9c6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9c6-110">-DefaultProfile</span></span>
<span data-ttu-id="ff9c6-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ff9c6-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff9c6-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="ff9c6-112">-LabName</span></span>
<span data-ttu-id="ff9c6-113">Annak a laboratóriumnak a nevét adja meg, amelynek a parancsmagja a virtuális gépek méretére vonatkozó házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="ff9c6-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="ff9c6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9c6-114">-ResourceGroupName</span></span>
<span data-ttu-id="ff9c6-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="ff9c6-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="ff9c6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9c6-116">CommonParameters</span></span>
<span data-ttu-id="ff9c6-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff9c6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9c6-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff9c6-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9c6-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff9c6-119">INPUTS</span></span>

### <span data-ttu-id="ff9c6-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ff9c6-120">System.String</span></span>

## <span data-ttu-id="ff9c6-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff9c6-121">OUTPUTS</span></span>

### <span data-ttu-id="ff9c6-122">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ff9c6-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="ff9c6-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff9c6-123">NOTES</span></span>

## <span data-ttu-id="ff9c6-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff9c6-124">RELATED LINKS</span></span>

[<span data-ttu-id="ff9c6-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ff9c6-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


