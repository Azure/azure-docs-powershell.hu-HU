---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 420226346f89b480c283a190ee54f87cde2de005
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670955"
---
# <span data-ttu-id="4688a-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="4688a-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="4688a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4688a-102">SYNOPSIS</span></span>
<span data-ttu-id="4688a-103">Beilleszti az engedélyezett virtuálisgép-méretekre vonatkozó házirendet a DevTest Labs szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="4688a-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="4688a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4688a-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4688a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4688a-105">DESCRIPTION</span></span>
<span data-ttu-id="4688a-106">A **Get-AzDtlAllowedVMSizesPolicy** parancsmag az engedélyezett virtuálisgép-méretekre vonatkozó házirendet kapja meg, amely lehetővé teszi, hogy megadhatja a laboratóriumban engedélyezett virtuális gépek méretének listáját.</span><span class="sxs-lookup"><span data-stu-id="4688a-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="4688a-107">A parancsmag az engedélyezett vagy letiltott állapotot adja meg a házirendnek, valamint a megadott házirendben beállított összes virtuális számítógép méretének listáját.</span><span class="sxs-lookup"><span data-stu-id="4688a-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="4688a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4688a-108">EXAMPLES</span></span>

## <span data-ttu-id="4688a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4688a-109">PARAMETERS</span></span>

### <span data-ttu-id="4688a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4688a-110">-DefaultProfile</span></span>
<span data-ttu-id="4688a-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4688a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4688a-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="4688a-112">-LabName</span></span>
<span data-ttu-id="4688a-113">Annak a laboratóriumnak a nevét adja meg, amelynek a parancsmagja a virtuális gépek méretére vonatkozó házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="4688a-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="4688a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4688a-114">-ResourceGroupName</span></span>
<span data-ttu-id="4688a-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="4688a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="4688a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4688a-116">CommonParameters</span></span>
<span data-ttu-id="4688a-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4688a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4688a-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4688a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4688a-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4688a-119">INPUTS</span></span>

### <span data-ttu-id="4688a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="4688a-120">System.String</span></span>

## <span data-ttu-id="4688a-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4688a-121">OUTPUTS</span></span>

### <span data-ttu-id="4688a-122">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="4688a-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="4688a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4688a-123">NOTES</span></span>

## <span data-ttu-id="4688a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4688a-124">RELATED LINKS</span></span>

[<span data-ttu-id="4688a-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="4688a-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="4688a-126">Azure Development-tesztkörnyezet-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4688a-126">Azure Development Test Lab Cmdlets</span></span>](./Az.DevTestLabs.md)


