---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 29d887639dd88f85a24144a4482c40c2b7626c7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328828"
---
# <span data-ttu-id="d319e-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d319e-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="d319e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d319e-102">SYNOPSIS</span></span>
<span data-ttu-id="d319e-103">A DevTest Labs tesztelési laboratóriumi osztályának laboratóriumi szabályzata szerint beveszi a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="d319e-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="d319e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d319e-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d319e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d319e-105">DESCRIPTION</span></span>
<span data-ttu-id="d319e-106">A **Get-AzDtlVMsPerLabPolicy** parancsmag egy laboratóriumi házirend alapján kapja meg a virtuális gépeket, így meg lehet állítani a laboratóriumokban engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="d319e-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="d319e-107">A parancsmag visszaadja a házirend engedélyezett vagy letiltott állapotát, valamint a házirendben beállított laboratóriumban engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="d319e-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="d319e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d319e-108">EXAMPLES</span></span>

## <span data-ttu-id="d319e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d319e-109">PARAMETERS</span></span>

### <span data-ttu-id="d319e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d319e-110">-DefaultProfile</span></span>
<span data-ttu-id="d319e-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d319e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d319e-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d319e-112">-LabName</span></span>
<span data-ttu-id="d319e-113">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag a virtuális gépeket beveszi.</span><span class="sxs-lookup"><span data-stu-id="d319e-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="d319e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d319e-114">-ResourceGroupName</span></span>
<span data-ttu-id="d319e-115">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a laboratórium tartozik.</span><span class="sxs-lookup"><span data-stu-id="d319e-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d319e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d319e-116">CommonParameters</span></span>
<span data-ttu-id="d319e-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d319e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d319e-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d319e-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d319e-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d319e-119">INPUTS</span></span>

### <span data-ttu-id="d319e-120">System.String</span><span class="sxs-lookup"><span data-stu-id="d319e-120">System.String</span></span>

## <span data-ttu-id="d319e-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d319e-121">OUTPUTS</span></span>

### <span data-ttu-id="d319e-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d319e-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="d319e-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d319e-123">NOTES</span></span>

## <span data-ttu-id="d319e-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d319e-124">RELATED LINKS</span></span>

[<span data-ttu-id="d319e-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d319e-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


