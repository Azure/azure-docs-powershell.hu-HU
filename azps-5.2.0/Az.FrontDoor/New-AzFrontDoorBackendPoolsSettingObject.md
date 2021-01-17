---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326447"
---
# <span data-ttu-id="60500-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="60500-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="60500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60500-102">SYNOPSIS</span></span>
<span data-ttu-id="60500-103">PSBackendPoolsSetting objektumot hozhat létre a Front Door létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="60500-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="60500-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60500-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60500-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60500-105">DESCRIPTION</span></span>
<span data-ttu-id="60500-106">A **New-AzFrontDoorBackendpoolsSettingObject** parancsmag létrehoz egy új PSBackendPoolsSettings objektumot a Front Door létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="60500-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="60500-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60500-107">EXAMPLES</span></span>

### <span data-ttu-id="60500-108">1. példa: BackendPoolsSettings objektum létrehozása alapértelmezett beállításokkal</span><span class="sxs-lookup"><span data-stu-id="60500-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="60500-109">2. példa: BackendPoolsSettings objektum létrehozása felhasználó által megadott értékekkel</span><span class="sxs-lookup"><span data-stu-id="60500-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="60500-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60500-110">PARAMETERS</span></span>

### <span data-ttu-id="60500-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60500-111">-DefaultProfile</span></span>
<span data-ttu-id="60500-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60500-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60500-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="60500-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="60500-114">Kényszerítse-e a tanúsítványnév-ellenőrzést a HTTPS-kérelmeken az összes háttérkészletben.</span><span class="sxs-lookup"><span data-stu-id="60500-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="60500-115">Nincs hatása a nem HTTPS-ről való kérelmekre.</span><span class="sxs-lookup"><span data-stu-id="60500-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="60500-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="60500-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="60500-117">Időtúllépés küldése és fogadása a háttérnek való továbbítási kéréskor.</span><span class="sxs-lookup"><span data-stu-id="60500-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="60500-118">Az időkorlát elérésekor a kérés sikertelen lesz, és visszatér.</span><span class="sxs-lookup"><span data-stu-id="60500-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="60500-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60500-119">CommonParameters</span></span>
<span data-ttu-id="60500-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60500-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60500-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60500-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60500-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60500-122">INPUTS</span></span>

### <span data-ttu-id="60500-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="60500-123">None</span></span>

## <span data-ttu-id="60500-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60500-124">OUTPUTS</span></span>

### <span data-ttu-id="60500-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="60500-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="60500-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60500-126">NOTES</span></span>

## <span data-ttu-id="60500-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60500-127">RELATED LINKS</span></span>
