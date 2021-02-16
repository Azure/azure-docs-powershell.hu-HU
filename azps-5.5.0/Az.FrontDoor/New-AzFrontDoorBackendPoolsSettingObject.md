---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167571"
---
# <span data-ttu-id="46f5a-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="46f5a-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="46f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="46f5a-103">PSBackendPoolsSetting objektumot hozhat létre a Front Door létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="46f5a-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="46f5a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46f5a-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46f5a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="46f5a-106">A **New-AzFrontDoorBackendpoolsSettingObject** parancsmag létrehoz egy új PSBackendPoolsSettings objektumot a Front Door létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="46f5a-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="46f5a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46f5a-107">EXAMPLES</span></span>

### <span data-ttu-id="46f5a-108">1. példa: BackendPoolsSettings objektum létrehozása alapértelmezett beállításokkal</span><span class="sxs-lookup"><span data-stu-id="46f5a-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="46f5a-109">2. példa: BackendPoolsSettings objektum létrehozása felhasználó által megadott értékekkel</span><span class="sxs-lookup"><span data-stu-id="46f5a-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="46f5a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46f5a-110">PARAMETERS</span></span>

### <span data-ttu-id="46f5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f5a-111">-DefaultProfile</span></span>
<span data-ttu-id="46f5a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46f5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46f5a-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="46f5a-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="46f5a-114">Kényszerítse-e a tanúsítványnév-ellenőrzést a HTTPS-kérelmeken az összes háttérkészletben.</span><span class="sxs-lookup"><span data-stu-id="46f5a-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="46f5a-115">Nincs hatása a nem HTTPS-ről való kérelmekre.</span><span class="sxs-lookup"><span data-stu-id="46f5a-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="46f5a-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="46f5a-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="46f5a-117">Időtúllépés küldése és fogadása a háttérnek való továbbítási kéréskor.</span><span class="sxs-lookup"><span data-stu-id="46f5a-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="46f5a-118">Az időkorlát elérésekor a kérés sikertelen lesz, és visszatér.</span><span class="sxs-lookup"><span data-stu-id="46f5a-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="46f5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f5a-119">CommonParameters</span></span>
<span data-ttu-id="46f5a-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f5a-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46f5a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f5a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46f5a-122">INPUTS</span></span>

### <span data-ttu-id="46f5a-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="46f5a-123">None</span></span>

## <span data-ttu-id="46f5a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46f5a-124">OUTPUTS</span></span>

### <span data-ttu-id="46f5a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="46f5a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="46f5a-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46f5a-126">NOTES</span></span>

## <span data-ttu-id="46f5a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46f5a-127">RELATED LINKS</span></span>
