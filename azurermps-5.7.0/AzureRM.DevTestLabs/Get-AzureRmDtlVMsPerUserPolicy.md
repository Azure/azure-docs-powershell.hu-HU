---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 53afed94f9733c041df2c49ff1ec97a2fb8277f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494505"
---
# <span data-ttu-id="d7726-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="d7726-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="d7726-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7726-102">SYNOPSIS</span></span>
<span data-ttu-id="d7726-103">A DevTest Labs-ban egy Lab virtuális gép felhasználónként házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="d7726-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7726-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7726-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7726-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7726-105">DESCRIPTION</span></span>
<span data-ttu-id="d7726-106">A **Get-AzureRmDtlVMsPerUserPolicy** parancsmag egy tesztkörnyezetben a virtuális gépek felhasználónkénti házirendjében kapja meg, amely lehetővé teszi a felhasználónként engedélyezett virtuális gépek maximális számának beállítását.</span><span class="sxs-lookup"><span data-stu-id="d7726-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="d7726-107">A parancsmag az engedélyezett vagy letiltott állapotot adja meg, valamint azt, hogy a házirendben beállított felhasználónként legfeljebb hány virtuális gépet engedélyeztek.</span><span class="sxs-lookup"><span data-stu-id="d7726-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="d7726-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d7726-108">EXAMPLES</span></span>

## <span data-ttu-id="d7726-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7726-109">PARAMETERS</span></span>

### <span data-ttu-id="d7726-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7726-110">-DefaultProfile</span></span>
<span data-ttu-id="d7726-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7726-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7726-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d7726-112">-LabName</span></span>
<span data-ttu-id="d7726-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag a virtuális gépet felhasználónkénti házirendjében kapja.</span><span class="sxs-lookup"><span data-stu-id="d7726-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="d7726-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7726-114">-ResourceGroupName</span></span>
<span data-ttu-id="d7726-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="d7726-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d7726-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7726-116">CommonParameters</span></span>
<span data-ttu-id="d7726-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7726-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7726-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7726-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7726-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7726-119">INPUTS</span></span>

### <span data-ttu-id="d7726-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7726-120">None</span></span>
<span data-ttu-id="d7726-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d7726-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7726-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7726-122">OUTPUTS</span></span>

### <span data-ttu-id="d7726-123">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d7726-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="d7726-124">Ez a parancsmag azt a házirendet adja eredményül, amely megadja a laboratóriumban egy felhasználó által létrehozható virtuális gépek maximális számát.</span><span class="sxs-lookup"><span data-stu-id="d7726-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="d7726-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7726-125">NOTES</span></span>

## <span data-ttu-id="d7726-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7726-126">RELATED LINKS</span></span>

[<span data-ttu-id="d7726-127">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="d7726-127">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


