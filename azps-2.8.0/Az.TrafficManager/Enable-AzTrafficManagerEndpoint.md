---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 99915859798eba5acb78fc62a5a5c56cff2ce791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838350"
---
# <span data-ttu-id="23f94-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="23f94-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="23f94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23f94-102">SYNOPSIS</span></span>
<span data-ttu-id="23f94-103">Lehetővé teszi, hogy egy végpont a forgalomirányítási profilban legyen.</span><span class="sxs-lookup"><span data-stu-id="23f94-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="23f94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23f94-104">SYNTAX</span></span>

### <span data-ttu-id="23f94-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="23f94-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23f94-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="23f94-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23f94-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="23f94-107">DESCRIPTION</span></span>
<span data-ttu-id="23f94-108">Az **enable-AzTrafficManagerEndpoint** parancsmag engedélyezi az Azure Traffic Manager-profilok végpontját.</span><span class="sxs-lookup"><span data-stu-id="23f94-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="23f94-109">A pipeline operátor segítségével átadhatja a **TrafficManagerEndpoint** -objektumokat a parancsmagnak, vagy megadhat egy **TrafficManagerEndpoint** -objektumot a *TrafficManagerEndpoint* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="23f94-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="23f94-110">Azt is megteheti, hogy megadhatja a végpont nevét és típusát a *név* és a *típus* paraméterrel együtt, a *fájl* -és *ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="23f94-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="23f94-111">Példák</span><span class="sxs-lookup"><span data-stu-id="23f94-111">EXAMPLES</span></span>

### <span data-ttu-id="23f94-112">1. példa: végpont engedélyezése profilból</span><span class="sxs-lookup"><span data-stu-id="23f94-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="23f94-113">Ez a parancs engedélyezi a contoso nevű külső végpontot az erőforráscsoport ResourceGroup11 nevű ContosoProfile-profilban.</span><span class="sxs-lookup"><span data-stu-id="23f94-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="23f94-114">2. példa: végpont engedélyezése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="23f94-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="23f94-115">Ez a parancs a contoso nevű külső végpontot a ResourceGroup11 nevű ContosoProfile-profilból kapja.</span><span class="sxs-lookup"><span data-stu-id="23f94-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="23f94-116">A parancs ezután a végpontot átadja az **enable-AzTrafficManagerEndpoint** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="23f94-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23f94-117">Ez a parancsmag engedélyezi az adott végpontot.</span><span class="sxs-lookup"><span data-stu-id="23f94-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="23f94-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23f94-118">PARAMETERS</span></span>

### <span data-ttu-id="23f94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f94-119">-DefaultProfile</span></span>
<span data-ttu-id="23f94-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23f94-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23f94-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23f94-121">-Name</span></span>
<span data-ttu-id="23f94-122">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="23f94-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f94-123">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="23f94-123">-ProfileName</span></span>
<span data-ttu-id="23f94-124">Annak a forgalomirányító-profilnak a nevét adja meg, amelyben a parancsmag engedélyezi a végpontot.</span><span class="sxs-lookup"><span data-stu-id="23f94-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="23f94-125">Ha profilt szeretne beolvasni, használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="23f94-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f94-126">-ResourceGroupName</span></span>
<span data-ttu-id="23f94-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="23f94-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="23f94-128">Ez a parancsmag lehetővé teszi a forgalom-kezelő végpontját abban a csoportban, amelyre ez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="23f94-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f94-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="23f94-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="23f94-130">A forgalomirányítási végpontot adja meg, amelyre a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="23f94-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="23f94-131">**TrafficManagerEndpoint** objektum beolvasásához használja az Get-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="23f94-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23f94-132">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="23f94-132">-Type</span></span>
<span data-ttu-id="23f94-133">Azt adja meg, hogy a parancsmag milyen típusú végpontot Tilt le a forgalomirányítási profilban.</span><span class="sxs-lookup"><span data-stu-id="23f94-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="23f94-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="23f94-134">Valid values are:</span></span> 

- <span data-ttu-id="23f94-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="23f94-135">AzureEndpoints</span></span>
- <span data-ttu-id="23f94-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="23f94-136">ExternalEndpoints</span></span>
- <span data-ttu-id="23f94-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="23f94-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f94-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f94-138">CommonParameters</span></span>
<span data-ttu-id="23f94-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23f94-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f94-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f94-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f94-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23f94-141">INPUTS</span></span>

### <span data-ttu-id="23f94-142">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="23f94-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="23f94-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23f94-143">OUTPUTS</span></span>

### <span data-ttu-id="23f94-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23f94-144">System.Boolean</span></span>

## <span data-ttu-id="23f94-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23f94-145">NOTES</span></span>

## <span data-ttu-id="23f94-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23f94-146">RELATED LINKS</span></span>

[<span data-ttu-id="23f94-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="23f94-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="23f94-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="23f94-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="23f94-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23f94-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="23f94-150">Új – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="23f94-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="23f94-151">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23f94-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="23f94-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="23f94-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="23f94-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23f94-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


