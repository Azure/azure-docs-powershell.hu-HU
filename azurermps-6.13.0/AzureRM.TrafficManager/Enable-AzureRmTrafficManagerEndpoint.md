---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 2556715c321ddcc3f8acbc518ddbe6a3048353af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495576"
---
# <span data-ttu-id="fe850-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe850-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="fe850-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe850-102">SYNOPSIS</span></span>
<span data-ttu-id="fe850-103">Lehetővé teszi, hogy egy végpont a forgalomirányítási profilban legyen.</span><span class="sxs-lookup"><span data-stu-id="fe850-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe850-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe850-104">SYNTAX</span></span>

### <span data-ttu-id="fe850-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="fe850-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe850-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="fe850-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe850-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe850-107">DESCRIPTION</span></span>
<span data-ttu-id="fe850-108">Az **enable-AzureRmTrafficManagerEndpoint** parancsmag engedélyezi az Azure Traffic Manager-profilok végpontját.</span><span class="sxs-lookup"><span data-stu-id="fe850-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="fe850-109">A pipeline operátor segítségével átadhatja a **TrafficManagerEndpoint** -objektumokat a parancsmagnak, vagy megadhat egy **TrafficManagerEndpoint** -objektumot a *TrafficManagerEndpoint* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="fe850-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="fe850-110">Azt is megteheti, hogy megadhatja a végpont nevét és típusát a *név* és a *típus* paraméterrel együtt, a *fájl* -és *ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="fe850-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="fe850-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fe850-111">EXAMPLES</span></span>

### <span data-ttu-id="fe850-112">1. példa: végpont engedélyezése profilból</span><span class="sxs-lookup"><span data-stu-id="fe850-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="fe850-113">Ez a parancs engedélyezi a contoso nevű külső végpontot az erőforráscsoport ResouceGroup11 nevű ContosoProfile-profilban.</span><span class="sxs-lookup"><span data-stu-id="fe850-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="fe850-114">2. példa: végpont engedélyezése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="fe850-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="fe850-115">Ez a parancs a contoso nevű külső végpontot a ResourceGroup11 nevű ContosoProfile-profilból kapja.</span><span class="sxs-lookup"><span data-stu-id="fe850-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="fe850-116">A parancs ezután a végpontot átadja az **enable-AzureRmTrafficManagerEndpoint** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="fe850-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fe850-117">Ez a parancsmag engedélyezi az adott végpontot.</span><span class="sxs-lookup"><span data-stu-id="fe850-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="fe850-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe850-118">PARAMETERS</span></span>

### <span data-ttu-id="fe850-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe850-119">-DefaultProfile</span></span>
<span data-ttu-id="fe850-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe850-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe850-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe850-121">-Name</span></span>
<span data-ttu-id="fe850-122">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="fe850-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="fe850-123">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="fe850-123">-ProfileName</span></span>
<span data-ttu-id="fe850-124">Annak a forgalomirányító-profilnak a nevét adja meg, amelyben a parancsmag engedélyezi a végpontot.</span><span class="sxs-lookup"><span data-stu-id="fe850-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="fe850-125">Ha profilt szeretne beolvasni, használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe850-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fe850-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe850-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe850-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe850-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fe850-128">Ez a parancsmag lehetővé teszi a forgalom-kezelő végpontját abban a csoportban, amelyre ez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="fe850-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe850-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe850-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="fe850-130">A forgalomirányítási végpontot adja meg, amelyre a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="fe850-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="fe850-131">**TrafficManagerEndpoint** objektum beolvasásához használja az Get-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe850-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="fe850-132">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="fe850-132">-Type</span></span>
<span data-ttu-id="fe850-133">Azt adja meg, hogy a parancsmag milyen típusú végpontot Tilt le a forgalomirányítási profilban.</span><span class="sxs-lookup"><span data-stu-id="fe850-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="fe850-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="fe850-134">Valid values are:</span></span> 

- <span data-ttu-id="fe850-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="fe850-135">AzureEndpoints</span></span>
- <span data-ttu-id="fe850-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="fe850-136">ExternalEndpoints</span></span>
- <span data-ttu-id="fe850-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="fe850-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="fe850-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe850-138">CommonParameters</span></span>
<span data-ttu-id="fe850-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe850-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe850-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe850-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe850-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe850-141">INPUTS</span></span>

### <span data-ttu-id="fe850-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe850-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="fe850-143">A ' TrafficManagerEndpoint ' paraméter az "TrafficManagerEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fe850-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="fe850-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe850-144">OUTPUTS</span></span>

### <span data-ttu-id="fe850-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe850-145">System.Boolean</span></span>

## <span data-ttu-id="fe850-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe850-146">NOTES</span></span>

## <span data-ttu-id="fe850-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe850-147">RELATED LINKS</span></span>

[<span data-ttu-id="fe850-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe850-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fe850-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe850-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fe850-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fe850-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fe850-151">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe850-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fe850-152">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fe850-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fe850-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe850-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fe850-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fe850-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


