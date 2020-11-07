---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 5cf730c5ba450978730617b7ddb270c0fdec2bf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836174"
---
# <span data-ttu-id="1649a-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="1649a-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="1649a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1649a-102">SYNOPSIS</span></span>
<span data-ttu-id="1649a-103">PSBackend objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="1649a-103">Create a PSBackend object</span></span>

## <span data-ttu-id="1649a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1649a-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1649a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1649a-105">DESCRIPTION</span></span>
<span data-ttu-id="1649a-106">PSBackend objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="1649a-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="1649a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1649a-107">EXAMPLES</span></span>

### <span data-ttu-id="1649a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1649a-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="1649a-109">PSBackend objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="1649a-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="1649a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1649a-110">PARAMETERS</span></span>

### <span data-ttu-id="1649a-111">-Address (cím)</span><span class="sxs-lookup"><span data-stu-id="1649a-111">-Address</span></span>
<span data-ttu-id="1649a-112">A backend (IP-cím vagy FQDN) helye</span><span class="sxs-lookup"><span data-stu-id="1649a-112">Location of the backend (IP address or FQDN)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1649a-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="1649a-113">-BackendHostHeader</span></span>
<span data-ttu-id="1649a-114">Az állomásfejléc által a backend-nek küldendő érték.</span><span class="sxs-lookup"><span data-stu-id="1649a-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="1649a-115">Az alapértelmezett érték a backend-cím.</span><span class="sxs-lookup"><span data-stu-id="1649a-115">Default value is the backend address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1649a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1649a-116">-DefaultProfile</span></span>
<span data-ttu-id="1649a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1649a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1649a-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="1649a-118">-EnabledState</span></span>
<span data-ttu-id="1649a-119">Engedélyezi-e a backend használatát.</span><span class="sxs-lookup"><span data-stu-id="1649a-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="1649a-120">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="1649a-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="1649a-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="1649a-121">-HttpPort</span></span>
<span data-ttu-id="1649a-122">A HTTP TCP-port száma</span><span class="sxs-lookup"><span data-stu-id="1649a-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="1649a-123">1 és 65535 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1649a-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="1649a-124">Az alapértelmezett érték a 80.</span><span class="sxs-lookup"><span data-stu-id="1649a-124">Default value is 80.</span></span>

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

### <span data-ttu-id="1649a-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="1649a-125">-HttpsPort</span></span>
<span data-ttu-id="1649a-126">A HTTPS TCP-port száma</span><span class="sxs-lookup"><span data-stu-id="1649a-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="1649a-127">1 és 65535 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1649a-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="1649a-128">Az alapértelmezett érték a 443</span><span class="sxs-lookup"><span data-stu-id="1649a-128">Default value is 443</span></span>

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

### <span data-ttu-id="1649a-129">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="1649a-129">-Priority</span></span>
<span data-ttu-id="1649a-130">A terheléselosztáshoz használható prioritás.</span><span class="sxs-lookup"><span data-stu-id="1649a-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="1649a-131">1 és 5 közöttinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1649a-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="1649a-132">Az alapértelmezett érték 1</span><span class="sxs-lookup"><span data-stu-id="1649a-132">Default value is 1</span></span>

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

### <span data-ttu-id="1649a-133">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="1649a-133">-Weight</span></span>
<span data-ttu-id="1649a-134">A végpont súlya a terheléselosztási célokra</span><span class="sxs-lookup"><span data-stu-id="1649a-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="1649a-135">1 és 1000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1649a-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="1649a-136">Az alapértelmezett érték a 50</span><span class="sxs-lookup"><span data-stu-id="1649a-136">Default value is 50</span></span>

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

### <span data-ttu-id="1649a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1649a-137">CommonParameters</span></span>
<span data-ttu-id="1649a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1649a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1649a-139">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1649a-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1649a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1649a-140">INPUTS</span></span>

### <span data-ttu-id="1649a-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="1649a-141">None</span></span>

## <span data-ttu-id="1649a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1649a-142">OUTPUTS</span></span>

### <span data-ttu-id="1649a-143">Microsoft. Azure. Command. FrontDoor. models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="1649a-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="1649a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1649a-144">NOTES</span></span>

## <span data-ttu-id="1649a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1649a-145">RELATED LINKS</span></span>

[<span data-ttu-id="1649a-146">Új – AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="1649a-146">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
