---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017641"
---
# <span data-ttu-id="51320-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="51320-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="51320-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51320-102">SYNOPSIS</span></span>
<span data-ttu-id="51320-103">Egy Application Control VM/Server csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="51320-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="51320-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51320-104">SYNTAX</span></span>

### <span data-ttu-id="51320-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51320-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51320-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="51320-106">DESCRIPTION</span></span>
<span data-ttu-id="51320-107">Az Azure Security Center automatikusan számítja ki az adaptív alkalmazások vezérlőit, ezt a parancsmagot használva beszerezhet egy Application Control VM/Server csoportot.</span><span class="sxs-lookup"><span data-stu-id="51320-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="51320-108">Példák</span><span class="sxs-lookup"><span data-stu-id="51320-108">EXAMPLES</span></span>

### <span data-ttu-id="51320-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="51320-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="51320-110">Egy Application Control VM/Server csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="51320-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="51320-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51320-111">PARAMETERS</span></span>

### <span data-ttu-id="51320-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51320-112">-DefaultProfile</span></span>
<span data-ttu-id="51320-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51320-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51320-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="51320-114">-AscLocation</span></span>
<span data-ttu-id="51320-115">Az a hely, ahol a ASC tárolja az előfizetés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="51320-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="51320-116">beolvasható a helyek beolvasása lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="51320-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51320-117">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="51320-117">-GroupName</span></span>
<span data-ttu-id="51320-118">Egy Application Control VM/Server csoport neve.</span><span class="sxs-lookup"><span data-stu-id="51320-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51320-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51320-119">-SubscriptionId</span></span>
<span data-ttu-id="51320-120">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="51320-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="51320-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51320-121">CommonParameters</span></span>
<span data-ttu-id="51320-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51320-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51320-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51320-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51320-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51320-124">INPUTS</span></span>

### <span data-ttu-id="51320-125">System. String</span><span class="sxs-lookup"><span data-stu-id="51320-125">System.String</span></span>

## <span data-ttu-id="51320-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51320-126">OUTPUTS</span></span>

### <span data-ttu-id="51320-127">Microsoft. Azure. commands. Security. models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="51320-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="51320-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51320-128">NOTES</span></span>

## <span data-ttu-id="51320-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51320-129">RELATED LINKS</span></span>