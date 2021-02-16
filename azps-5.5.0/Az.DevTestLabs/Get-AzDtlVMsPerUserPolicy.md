---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167667"
---
# <span data-ttu-id="01c06-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="01c06-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="01c06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c06-102">SYNOPSIS</span></span>
<span data-ttu-id="01c06-103">A DevTest Labs tesztelési laboratóriumának felhasználónkénti házirendet használó virtuális gépeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="01c06-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="01c06-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01c06-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01c06-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01c06-105">DESCRIPTION</span></span>
<span data-ttu-id="01c06-106">A **Get-AzDtlVMsPerUserPolicy** parancsmag egy lab felhasználónkénti házirendjére beveszi a virtuális gépeket, amely lehetővé teszi a felhasználónként engedélyezett virtuális gépek maximális számának beállítását.</span><span class="sxs-lookup"><span data-stu-id="01c06-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="01c06-107">A parancsmag visszaadja a házirend engedélyezett vagy letiltott állapotát, valamint a házirendben felhasználónként engedélyezett virtuális gépek maximális számát.</span><span class="sxs-lookup"><span data-stu-id="01c06-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="01c06-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01c06-108">EXAMPLES</span></span>

## <span data-ttu-id="01c06-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01c06-109">PARAMETERS</span></span>

### <span data-ttu-id="01c06-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c06-110">-DefaultProfile</span></span>
<span data-ttu-id="01c06-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="01c06-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01c06-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="01c06-112">-LabName</span></span>
<span data-ttu-id="01c06-113">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag felhasználónkénti házirendenként virtuális gépet kap.</span><span class="sxs-lookup"><span data-stu-id="01c06-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="01c06-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c06-114">-ResourceGroupName</span></span>
<span data-ttu-id="01c06-115">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a laboratórium tartozik.</span><span class="sxs-lookup"><span data-stu-id="01c06-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="01c06-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c06-116">CommonParameters</span></span>
<span data-ttu-id="01c06-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c06-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c06-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c06-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c06-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01c06-119">INPUTS</span></span>

### <span data-ttu-id="01c06-120">System.String</span><span class="sxs-lookup"><span data-stu-id="01c06-120">System.String</span></span>

## <span data-ttu-id="01c06-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01c06-121">OUTPUTS</span></span>

### <span data-ttu-id="01c06-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="01c06-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="01c06-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01c06-123">NOTES</span></span>

## <span data-ttu-id="01c06-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01c06-124">RELATED LINKS</span></span>

[<span data-ttu-id="01c06-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="01c06-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


