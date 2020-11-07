---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845506"
---
# <span data-ttu-id="a7237-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="a7237-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="a7237-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7237-102">SYNOPSIS</span></span>
<span data-ttu-id="a7237-103">PSBackendPoolsSetting objektum létrehozása az első ajtó létrehozása céljából.</span><span class="sxs-lookup"><span data-stu-id="a7237-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="a7237-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7237-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7237-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7237-105">DESCRIPTION</span></span>
<span data-ttu-id="a7237-106">A **New-AzFrontDoorBackendpoolsSettingObject** parancsmag új PSBackendPoolsSettings objektumot hoz létre a bejárati ajtó létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a7237-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="a7237-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a7237-107">EXAMPLES</span></span>

### <span data-ttu-id="a7237-108">1. példa: BackendPoolsSettings-objektum létrehozása alapértelmezett beállításokkal</span><span class="sxs-lookup"><span data-stu-id="a7237-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="a7237-109">2. példa: BackendPoolsSettings objektum létrehozása a felhasználó által megadott értékekkel</span><span class="sxs-lookup"><span data-stu-id="a7237-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="a7237-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7237-110">PARAMETERS</span></span>

### <span data-ttu-id="a7237-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7237-111">-DefaultProfile</span></span>
<span data-ttu-id="a7237-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7237-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7237-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="a7237-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="a7237-114">Engedélyezi-e a tanúsítvány nevének érvényesítését HTTPS-kérések esetén az összes backend-készletre.</span><span class="sxs-lookup"><span data-stu-id="a7237-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="a7237-115">Nincs hatással a nem HTTPS-kérésekre.</span><span class="sxs-lookup"><span data-stu-id="a7237-115">No effect on non-HTTPS requests.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7237-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="a7237-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="a7237-117">Küldési és fogadási időtúllépés a háttérben való továbbítás kérése során.</span><span class="sxs-lookup"><span data-stu-id="a7237-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="a7237-118">Az időtúllépés elérésekor a kérés nem sikerül, és a visszatérési érték.</span><span class="sxs-lookup"><span data-stu-id="a7237-118">When timeout is reached, the request fails and returns.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7237-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7237-119">CommonParameters</span></span>
<span data-ttu-id="a7237-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7237-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7237-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a7237-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7237-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7237-122">INPUTS</span></span>

### <span data-ttu-id="a7237-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="a7237-123">None</span></span>

## <span data-ttu-id="a7237-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7237-124">OUTPUTS</span></span>

### <span data-ttu-id="a7237-125">Microsoft. Azure. Command. FrontDoor. models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="a7237-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="a7237-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7237-126">NOTES</span></span>

## <span data-ttu-id="a7237-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7237-127">RELATED LINKS</span></span>
