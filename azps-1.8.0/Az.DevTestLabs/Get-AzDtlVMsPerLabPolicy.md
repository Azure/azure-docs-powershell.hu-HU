---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 2603a9c5f259de05b466693bdc42d7a6dfb2eda2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670948"
---
# <span data-ttu-id="f03e5-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="f03e5-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="f03e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f03e5-102">SYNOPSIS</span></span>
<span data-ttu-id="f03e5-103">Az DevTest Labs-ban egy laborban lévő virtuális gépekre vonatkozó házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="f03e5-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="f03e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f03e5-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f03e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f03e5-105">DESCRIPTION</span></span>
<span data-ttu-id="f03e5-106">A **Get-AzDtlVMsPerLabPolicy** parancsmag a laboratóriumok egy Lab-házirendjéhez tartozó virtuális gépeket kapja meg, amely lehetővé teszi a tesztkörnyezetben engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="f03e5-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="f03e5-107">A parancsmag az engedélyezett vagy letiltott állapotot adja eredményül, valamint a házirendben beállított laboratóriumban engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="f03e5-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="f03e5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f03e5-108">EXAMPLES</span></span>

## <span data-ttu-id="f03e5-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f03e5-109">PARAMETERS</span></span>

### <span data-ttu-id="f03e5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03e5-110">-DefaultProfile</span></span>
<span data-ttu-id="f03e5-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f03e5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f03e5-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="f03e5-112">-LabName</span></span>
<span data-ttu-id="f03e5-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag a virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="f03e5-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="f03e5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03e5-114">-ResourceGroupName</span></span>
<span data-ttu-id="f03e5-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="f03e5-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="f03e5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03e5-116">CommonParameters</span></span>
<span data-ttu-id="f03e5-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f03e5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03e5-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f03e5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03e5-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f03e5-119">INPUTS</span></span>

### <span data-ttu-id="f03e5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f03e5-120">System.String</span></span>

## <span data-ttu-id="f03e5-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f03e5-121">OUTPUTS</span></span>

### <span data-ttu-id="f03e5-122">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f03e5-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="f03e5-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f03e5-123">NOTES</span></span>

## <span data-ttu-id="f03e5-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f03e5-124">RELATED LINKS</span></span>

[<span data-ttu-id="f03e5-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="f03e5-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


