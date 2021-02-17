---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155658"
---
# <span data-ttu-id="f82f1-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="f82f1-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="f82f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f82f1-102">SYNOPSIS</span></span>
<span data-ttu-id="f82f1-103">PSBackend-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="f82f1-103">Create a PSBackend object</span></span>

## <span data-ttu-id="f82f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f82f1-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f82f1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f82f1-105">DESCRIPTION</span></span>
<span data-ttu-id="f82f1-106">PSBackend-objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f82f1-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="f82f1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f82f1-107">EXAMPLES</span></span>

### <span data-ttu-id="f82f1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f82f1-108">Example 1</span></span>
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

<span data-ttu-id="f82f1-109">PSBackend-objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f82f1-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="f82f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f82f1-110">PARAMETERS</span></span>

### <span data-ttu-id="f82f1-111">-Address</span><span class="sxs-lookup"><span data-stu-id="f82f1-111">-Address</span></span>
<span data-ttu-id="f82f1-112">A háttérhálózat helye (IP-cím vagy teljes tartomány neve)</span><span class="sxs-lookup"><span data-stu-id="f82f1-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="f82f1-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="f82f1-113">-BackendHostHeader</span></span>
<span data-ttu-id="f82f1-114">A háttérnek küldött állomásfejlécként használt érték.</span><span class="sxs-lookup"><span data-stu-id="f82f1-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="f82f1-115">Az alapértelmezett érték a háttércím.</span><span class="sxs-lookup"><span data-stu-id="f82f1-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="f82f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f82f1-116">-DefaultProfile</span></span>
<span data-ttu-id="f82f1-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f82f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f82f1-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f82f1-118">-EnabledState</span></span>
<span data-ttu-id="f82f1-119">Eldönti, hogy engedélyezi-e ennek a háttérnek a használatát.</span><span class="sxs-lookup"><span data-stu-id="f82f1-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="f82f1-120">Az alapértelmezett érték engedélyezve van</span><span class="sxs-lookup"><span data-stu-id="f82f1-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="f82f1-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="f82f1-121">-HttpPort</span></span>
<span data-ttu-id="f82f1-122">A HTTP TCP-port száma.</span><span class="sxs-lookup"><span data-stu-id="f82f1-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="f82f1-123">1 és 65535 közé kell esnie.</span><span class="sxs-lookup"><span data-stu-id="f82f1-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="f82f1-124">Az alapértelmezett érték 80.</span><span class="sxs-lookup"><span data-stu-id="f82f1-124">Default value is 80.</span></span>

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

### <span data-ttu-id="f82f1-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="f82f1-125">-HttpsPort</span></span>
<span data-ttu-id="f82f1-126">A HTTPS TCP-port száma.</span><span class="sxs-lookup"><span data-stu-id="f82f1-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="f82f1-127">1 és 65535 közé kell esnie.</span><span class="sxs-lookup"><span data-stu-id="f82f1-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="f82f1-128">Az alapértelmezett érték 443</span><span class="sxs-lookup"><span data-stu-id="f82f1-128">Default value is 443</span></span>

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

### <span data-ttu-id="f82f1-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="f82f1-129">-Priority</span></span>
<span data-ttu-id="f82f1-130">A terheléselosztáshoz használt prioritás.</span><span class="sxs-lookup"><span data-stu-id="f82f1-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="f82f1-131">1 és 5 közé kell esnie.</span><span class="sxs-lookup"><span data-stu-id="f82f1-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="f82f1-132">Az alapértelmezett érték 1</span><span class="sxs-lookup"><span data-stu-id="f82f1-132">Default value is 1</span></span>

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

### <span data-ttu-id="f82f1-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="f82f1-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="f82f1-134">A Privát hivatkozás erőforrás aliasa.</span><span class="sxs-lookup"><span data-stu-id="f82f1-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="f82f1-135">A nem kötelező mező kitöltése azt jelzi, hogy a háttérhálózat "Privát"</span><span class="sxs-lookup"><span data-stu-id="f82f1-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="f82f1-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="f82f1-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="f82f1-137">A személyes hivatkozáshoz való csatlakozáshoz a jóváhagyási kérelemben szerepelni fog egy egyéni üzenet</span><span class="sxs-lookup"><span data-stu-id="f82f1-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="f82f1-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="f82f1-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="f82f1-139">The Location of Private Link resource.</span><span class="sxs-lookup"><span data-stu-id="f82f1-139">The Location of Private Link resource.</span></span> <span data-ttu-id="f82f1-140">Hely szükséges a PrivateLinkResourceId beállításakor</span><span class="sxs-lookup"><span data-stu-id="f82f1-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="f82f1-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f82f1-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f82f1-142">A magánjellegű hivatkozás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f82f1-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="f82f1-143">A nem kötelező mező kitöltése azt jelzi, hogy a háttérhálózat "Privát"</span><span class="sxs-lookup"><span data-stu-id="f82f1-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="f82f1-144">-Weight</span><span class="sxs-lookup"><span data-stu-id="f82f1-144">-Weight</span></span>
<span data-ttu-id="f82f1-145">A végpont súlyozása terheléselosztási célokra.</span><span class="sxs-lookup"><span data-stu-id="f82f1-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="f82f1-146">1 és 1000 közé kell esnie.</span><span class="sxs-lookup"><span data-stu-id="f82f1-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="f82f1-147">Az alapértelmezett érték 50</span><span class="sxs-lookup"><span data-stu-id="f82f1-147">Default value is 50</span></span>

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

### <span data-ttu-id="f82f1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f82f1-148">CommonParameters</span></span>
<span data-ttu-id="f82f1-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f82f1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f82f1-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f82f1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f82f1-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f82f1-151">INPUTS</span></span>

### <span data-ttu-id="f82f1-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="f82f1-152">None</span></span>

## <span data-ttu-id="f82f1-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f82f1-153">OUTPUTS</span></span>

### <span data-ttu-id="f82f1-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="f82f1-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="f82f1-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f82f1-155">NOTES</span></span>

## <span data-ttu-id="f82f1-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f82f1-156">RELATED LINKS</span></span>

[<span data-ttu-id="f82f1-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="f82f1-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
