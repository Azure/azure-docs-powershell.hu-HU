---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467849"
---
# <span data-ttu-id="18fbc-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="18fbc-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="18fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="18fbc-103">A DevTest Labs által engedélyezett virtuális gépméretekre vonatkozó házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="18fbc-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="18fbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18fbc-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18fbc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="18fbc-106">A **Get-AzDtlAllowedVMSizesPolicy** parancsmag megkapja az engedélyezett virtuális gépméretekre vonatkozó házirendet, amely lehetővé teszi a laboratóriumban engedélyezett virtuális gépméretek listájának megadását.</span><span class="sxs-lookup"><span data-stu-id="18fbc-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="18fbc-107">A parancsmag visszaadja a házirend engedélyezett vagy letiltott állapotát, valamint a megadott házirendben beállított összes engedélyezett virtuális gépméret listáját.</span><span class="sxs-lookup"><span data-stu-id="18fbc-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="18fbc-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18fbc-108">EXAMPLES</span></span>

## <span data-ttu-id="18fbc-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18fbc-109">PARAMETERS</span></span>

### <span data-ttu-id="18fbc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fbc-110">-DefaultProfile</span></span>
<span data-ttu-id="18fbc-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="18fbc-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18fbc-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="18fbc-112">-LabName</span></span>
<span data-ttu-id="18fbc-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag virtuális gépméret-házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="18fbc-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="18fbc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fbc-114">-ResourceGroupName</span></span>
<span data-ttu-id="18fbc-115">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a laboratórium tartozik.</span><span class="sxs-lookup"><span data-stu-id="18fbc-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="18fbc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fbc-116">CommonParameters</span></span>
<span data-ttu-id="18fbc-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18fbc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fbc-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18fbc-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fbc-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18fbc-119">INPUTS</span></span>

### <span data-ttu-id="18fbc-120">System.String</span><span class="sxs-lookup"><span data-stu-id="18fbc-120">System.String</span></span>

## <span data-ttu-id="18fbc-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18fbc-121">OUTPUTS</span></span>

### <span data-ttu-id="18fbc-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="18fbc-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="18fbc-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18fbc-123">NOTES</span></span>

## <span data-ttu-id="18fbc-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18fbc-124">RELATED LINKS</span></span>

[<span data-ttu-id="18fbc-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="18fbc-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


