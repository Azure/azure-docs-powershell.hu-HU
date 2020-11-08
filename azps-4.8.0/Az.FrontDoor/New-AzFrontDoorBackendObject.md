---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183579"
---
# <span data-ttu-id="84a4d-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="84a4d-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="84a4d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="84a4d-103">PSBackend objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="84a4d-103">Create a PSBackend object</span></span>

## <span data-ttu-id="84a4d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84a4d-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84a4d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="84a4d-106">PSBackend objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="84a4d-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="84a4d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="84a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="84a4d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="84a4d-108">Example 1</span></span>
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

<span data-ttu-id="84a4d-109">PSBackend objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="84a4d-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="84a4d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84a4d-110">PARAMETERS</span></span>

### <span data-ttu-id="84a4d-111">-Address (cím)</span><span class="sxs-lookup"><span data-stu-id="84a4d-111">-Address</span></span>
<span data-ttu-id="84a4d-112">A backend (IP-cím vagy FQDN) helye</span><span class="sxs-lookup"><span data-stu-id="84a4d-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="84a4d-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="84a4d-113">-BackendHostHeader</span></span>
<span data-ttu-id="84a4d-114">Az állomásfejléc által a backend-nek küldendő érték.</span><span class="sxs-lookup"><span data-stu-id="84a4d-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="84a4d-115">Az alapértelmezett érték a backend-cím.</span><span class="sxs-lookup"><span data-stu-id="84a4d-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="84a4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a4d-116">-DefaultProfile</span></span>
<span data-ttu-id="84a4d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84a4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a4d-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="84a4d-118">-EnabledState</span></span>
<span data-ttu-id="84a4d-119">Engedélyezi-e a backend használatát.</span><span class="sxs-lookup"><span data-stu-id="84a4d-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="84a4d-120">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="84a4d-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="84a4d-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="84a4d-121">-HttpPort</span></span>
<span data-ttu-id="84a4d-122">A HTTP TCP-port száma</span><span class="sxs-lookup"><span data-stu-id="84a4d-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="84a4d-123">1 és 65535 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84a4d-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="84a4d-124">Az alapértelmezett érték a 80.</span><span class="sxs-lookup"><span data-stu-id="84a4d-124">Default value is 80.</span></span>

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

### <span data-ttu-id="84a4d-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="84a4d-125">-HttpsPort</span></span>
<span data-ttu-id="84a4d-126">A HTTPS TCP-port száma</span><span class="sxs-lookup"><span data-stu-id="84a4d-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="84a4d-127">1 és 65535 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84a4d-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="84a4d-128">Az alapértelmezett érték a 443</span><span class="sxs-lookup"><span data-stu-id="84a4d-128">Default value is 443</span></span>

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

### <span data-ttu-id="84a4d-129">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="84a4d-129">-Priority</span></span>
<span data-ttu-id="84a4d-130">A terheléselosztáshoz használható prioritás.</span><span class="sxs-lookup"><span data-stu-id="84a4d-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="84a4d-131">1 és 5 közöttinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84a4d-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="84a4d-132">Az alapértelmezett érték 1</span><span class="sxs-lookup"><span data-stu-id="84a4d-132">Default value is 1</span></span>

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

### <span data-ttu-id="84a4d-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="84a4d-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="84a4d-134">A magánjellegű hivatkozás erőforrás aliasa.</span><span class="sxs-lookup"><span data-stu-id="84a4d-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="84a4d-135">A nem kötelező mező kitöltése azt jelzi, hogy ez a backend "Private"</span><span class="sxs-lookup"><span data-stu-id="84a4d-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="84a4d-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="84a4d-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="84a4d-137">A privát hivatkozáshoz való csatlakozáshoz a jóváhagyási kérelemben szerepeltetni kívánt egyéni üzenet</span><span class="sxs-lookup"><span data-stu-id="84a4d-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="84a4d-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="84a4d-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="84a4d-139">A magánjellegű hivatkozás erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="84a4d-139">The Location of Private Link resource.</span></span> <span data-ttu-id="84a4d-140">A PrivateLinkResourceId beállításakor a hely szükséges</span><span class="sxs-lookup"><span data-stu-id="84a4d-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="84a4d-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="84a4d-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="84a4d-142">A magánjellegű hivatkozás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="84a4d-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="84a4d-143">A nem kötelező mező kitöltése azt jelzi, hogy ez a backend "Private"</span><span class="sxs-lookup"><span data-stu-id="84a4d-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="84a4d-144">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="84a4d-144">-Weight</span></span>
<span data-ttu-id="84a4d-145">A végpont súlya a terheléselosztási célokra</span><span class="sxs-lookup"><span data-stu-id="84a4d-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="84a4d-146">1 és 1000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84a4d-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="84a4d-147">Az alapértelmezett érték a 50</span><span class="sxs-lookup"><span data-stu-id="84a4d-147">Default value is 50</span></span>

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

### <span data-ttu-id="84a4d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a4d-148">CommonParameters</span></span>
<span data-ttu-id="84a4d-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84a4d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a4d-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="84a4d-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a4d-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84a4d-151">INPUTS</span></span>

### <span data-ttu-id="84a4d-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="84a4d-152">None</span></span>

## <span data-ttu-id="84a4d-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84a4d-153">OUTPUTS</span></span>

### <span data-ttu-id="84a4d-154">Microsoft. Azure. Command. FrontDoor. models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="84a4d-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="84a4d-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84a4d-155">NOTES</span></span>

## <span data-ttu-id="84a4d-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84a4d-156">RELATED LINKS</span></span>

[<span data-ttu-id="84a4d-157">Új – AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="84a4d-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
