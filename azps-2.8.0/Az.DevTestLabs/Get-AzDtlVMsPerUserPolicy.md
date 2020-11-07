---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 3a3106dc400345b3debddc54cc9a9f8fdfd8f816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666607"
---
# <span data-ttu-id="03a28-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="03a28-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="03a28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03a28-102">SYNOPSIS</span></span>
<span data-ttu-id="03a28-103">A DevTest Labs-ban egy Lab virtuális gép felhasználónként házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="03a28-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="03a28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03a28-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03a28-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03a28-105">DESCRIPTION</span></span>
<span data-ttu-id="03a28-106">A **Get-AzDtlVMsPerUserPolicy** parancsmag egy tesztkörnyezetben a virtuális gépek felhasználónkénti házirendjében kapja meg, amely lehetővé teszi a felhasználónként engedélyezett virtuális gépek maximális számának beállítását.</span><span class="sxs-lookup"><span data-stu-id="03a28-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="03a28-107">A parancsmag az engedélyezett vagy letiltott állapotot adja meg, valamint azt, hogy a házirendben beállított felhasználónként legfeljebb hány virtuális gépet engedélyeztek.</span><span class="sxs-lookup"><span data-stu-id="03a28-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="03a28-108">Példák</span><span class="sxs-lookup"><span data-stu-id="03a28-108">EXAMPLES</span></span>

## <span data-ttu-id="03a28-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03a28-109">PARAMETERS</span></span>

### <span data-ttu-id="03a28-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a28-110">-DefaultProfile</span></span>
<span data-ttu-id="03a28-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="03a28-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03a28-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="03a28-112">-LabName</span></span>
<span data-ttu-id="03a28-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag a virtuális gépet felhasználónkénti házirendjében kapja.</span><span class="sxs-lookup"><span data-stu-id="03a28-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="03a28-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a28-114">-ResourceGroupName</span></span>
<span data-ttu-id="03a28-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="03a28-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="03a28-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a28-116">CommonParameters</span></span>
<span data-ttu-id="03a28-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03a28-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a28-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a28-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a28-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03a28-119">INPUTS</span></span>

### <span data-ttu-id="03a28-120">System. String</span><span class="sxs-lookup"><span data-stu-id="03a28-120">System.String</span></span>

## <span data-ttu-id="03a28-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03a28-121">OUTPUTS</span></span>

### <span data-ttu-id="03a28-122">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="03a28-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="03a28-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03a28-123">NOTES</span></span>

## <span data-ttu-id="03a28-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03a28-124">RELATED LINKS</span></span>

[<span data-ttu-id="03a28-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="03a28-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


