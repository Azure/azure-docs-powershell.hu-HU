---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 83b061c646d8d6f75689d6a67fe163c43456edb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495375"
---
# <span data-ttu-id="0ed3c-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="0ed3c-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="0ed3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ed3c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed3c-103">Az DevTest Labs-ban egy laborban lévő virtuális gépekre vonatkozó házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ed3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ed3c-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ed3c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ed3c-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed3c-106">A **Get-AzureRmDtlVMsPerLabPolicy** parancsmag a laboratóriumok egy Lab-házirendjéhez tartozó virtuális gépeket kapja meg, amely lehetővé teszi a tesztkörnyezetben engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="0ed3c-107">A parancsmag az engedélyezett vagy letiltott állapotot adja eredményül, valamint a házirendben beállított laboratóriumban engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="0ed3c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0ed3c-108">EXAMPLES</span></span>

## <span data-ttu-id="0ed3c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ed3c-109">PARAMETERS</span></span>

### <span data-ttu-id="0ed3c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed3c-110">-DefaultProfile</span></span>
<span data-ttu-id="0ed3c-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ed3c-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed3c-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="0ed3c-112">-LabName</span></span>
<span data-ttu-id="0ed3c-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag a virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed3c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed3c-114">-ResourceGroupName</span></span>
<span data-ttu-id="0ed3c-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed3c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed3c-116">CommonParameters</span></span>
<span data-ttu-id="0ed3c-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ed3c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed3c-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed3c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed3c-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ed3c-119">INPUTS</span></span>

### <span data-ttu-id="0ed3c-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ed3c-120">None</span></span>
<span data-ttu-id="0ed3c-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ed3c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ed3c-122">OUTPUTS</span></span>

### <span data-ttu-id="0ed3c-123">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0ed3c-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="0ed3c-124">Ez a parancsmag azt a házirendet adja eredményül, amely a laboratóriumban létrehozható virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="0ed3c-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ed3c-125">NOTES</span></span>

## <span data-ttu-id="0ed3c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ed3c-126">RELATED LINKS</span></span>

[<span data-ttu-id="0ed3c-127">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="0ed3c-127">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


