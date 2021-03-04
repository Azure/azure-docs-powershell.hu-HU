---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: fa19f45527302c858593d200fb2a6ed605d02321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930082"
---
# <span data-ttu-id="a810d-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a810d-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="a810d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a810d-102">SYNOPSIS</span></span>
<span data-ttu-id="a810d-103">A DevTest Labs tesztelési laboratóriumi osztályának laboratóriumi szabályzata szerint beveszi a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="a810d-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="a810d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a810d-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a810d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a810d-105">DESCRIPTION</span></span>
<span data-ttu-id="a810d-106">A **Get-AzDtlVMsPerLabPolicy** parancsmag egy laboratóriumi házirend alapján kapja meg a virtuális gépeket, így meg lehet állítani a laboratóriumokban engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="a810d-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="a810d-107">A parancsmag visszaadja a házirend engedélyezett vagy letiltott állapotát, valamint a házirendben beállított laboratóriumban engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="a810d-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="a810d-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a810d-108">EXAMPLES</span></span>

## <span data-ttu-id="a810d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a810d-109">PARAMETERS</span></span>

### <span data-ttu-id="a810d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a810d-110">-DefaultProfile</span></span>
<span data-ttu-id="a810d-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a810d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a810d-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a810d-112">-LabName</span></span>
<span data-ttu-id="a810d-113">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag a virtuális gépeket beveszi.</span><span class="sxs-lookup"><span data-stu-id="a810d-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="a810d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a810d-114">-ResourceGroupName</span></span>
<span data-ttu-id="a810d-115">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a laboratórium tartozik.</span><span class="sxs-lookup"><span data-stu-id="a810d-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a810d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a810d-116">CommonParameters</span></span>
<span data-ttu-id="a810d-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a810d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a810d-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a810d-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a810d-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a810d-119">INPUTS</span></span>

### <span data-ttu-id="a810d-120">System.String</span><span class="sxs-lookup"><span data-stu-id="a810d-120">System.String</span></span>

## <span data-ttu-id="a810d-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a810d-121">OUTPUTS</span></span>

### <span data-ttu-id="a810d-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a810d-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a810d-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a810d-123">NOTES</span></span>

## <span data-ttu-id="a810d-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a810d-124">RELATED LINKS</span></span>

[<span data-ttu-id="a810d-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a810d-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


