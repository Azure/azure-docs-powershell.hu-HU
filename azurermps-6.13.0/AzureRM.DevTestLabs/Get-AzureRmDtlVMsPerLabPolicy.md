---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3f38c8ace41a1f125a37053f136cd61c597787ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495134"
---
# <span data-ttu-id="ce2c4-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="ce2c4-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="ce2c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ce2c4-103">Az DevTest Labs-ban egy laborban lévő virtuális gépekre vonatkozó házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce2c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce2c4-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce2c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce2c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ce2c4-106">A **Get-AzureRmDtlVMsPerLabPolicy** parancsmag a laboratóriumok egy Lab-házirendjéhez tartozó virtuális gépeket kapja meg, amely lehetővé teszi a tesztkörnyezetben engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="ce2c4-107">A parancsmag az engedélyezett vagy letiltott állapotot adja eredményül, valamint a házirendben beállított laboratóriumban engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="ce2c4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ce2c4-108">EXAMPLES</span></span>

## <span data-ttu-id="ce2c4-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce2c4-109">PARAMETERS</span></span>

### <span data-ttu-id="ce2c4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce2c4-110">-DefaultProfile</span></span>
<span data-ttu-id="ce2c4-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ce2c4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce2c4-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="ce2c4-112">-LabName</span></span>
<span data-ttu-id="ce2c4-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag a virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="ce2c4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce2c4-114">-ResourceGroupName</span></span>
<span data-ttu-id="ce2c4-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="ce2c4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce2c4-116">CommonParameters</span></span>
<span data-ttu-id="ce2c4-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce2c4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce2c4-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce2c4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce2c4-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce2c4-119">INPUTS</span></span>

### <span data-ttu-id="ce2c4-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ce2c4-120">System.String</span></span>

## <span data-ttu-id="ce2c4-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce2c4-121">OUTPUTS</span></span>

### <span data-ttu-id="ce2c4-122">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ce2c4-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="ce2c4-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce2c4-123">NOTES</span></span>

## <span data-ttu-id="ce2c4-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce2c4-124">RELATED LINKS</span></span>

[<span data-ttu-id="ce2c4-125">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="ce2c4-125">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


