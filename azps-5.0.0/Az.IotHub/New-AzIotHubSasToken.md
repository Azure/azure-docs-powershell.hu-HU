---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187735"
---
# <span data-ttu-id="f83c3-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="f83c3-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="f83c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f83c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f83c3-103">Hozzon létre egy SAS-tokent a TARGET IoT hub, eszköz vagy modul számára.</span><span class="sxs-lookup"><span data-stu-id="f83c3-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="f83c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f83c3-104">SYNTAX</span></span>

### <span data-ttu-id="f83c3-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f83c3-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f83c3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f83c3-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f83c3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f83c3-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f83c3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f83c3-108">DESCRIPTION</span></span>
<span data-ttu-id="f83c3-109">Az eszközök SAS-tokenei esetében a házirend paraméter csak az eszköz beállításjegyzékének elérésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f83c3-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="f83c3-110">Ezért a házirendnek olvasási jogosultsággal kell rendelkeznie a beállításjegyzékhez.</span><span class="sxs-lookup"><span data-stu-id="f83c3-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="f83c3-111">IoT hub-tokenek esetén a házirend a biztonsági társítás része.</span><span class="sxs-lookup"><span data-stu-id="f83c3-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="f83c3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f83c3-112">EXAMPLES</span></span>

### <span data-ttu-id="f83c3-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f83c3-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="f83c3-114">Hozzon létre egy IoT hub SAS-tokent a iothubowner házirend és az elsődleges kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="f83c3-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="f83c3-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="f83c3-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="f83c3-116">Hozzon létre egy IoT hub SAS-tokent a registryRead házirend és a másodlagos kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="f83c3-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="f83c3-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="f83c3-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="f83c3-118">Hozzon létre egy eszközt SAS-jogkivonatot a iothubowner házirenddel a {iothub_name} Device Registry eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f83c3-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="f83c3-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="f83c3-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="f83c3-120">Hozzon létre egy modult a SAS-token iothubowner házirenddel a {iothub_name} Device Registry eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f83c3-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="f83c3-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f83c3-121">PARAMETERS</span></span>

### <span data-ttu-id="f83c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83c3-122">-DefaultProfile</span></span>
<span data-ttu-id="f83c3-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f83c3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f83c3-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f83c3-124">-DeviceId</span></span>
<span data-ttu-id="f83c3-125">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f83c3-125">Target Device Id.</span></span>

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

### <span data-ttu-id="f83c3-126">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="f83c3-126">-Duration</span></span>
<span data-ttu-id="f83c3-127">A létrehozandó jogkivonat lejárati ideje (másodpercben)</span><span class="sxs-lookup"><span data-stu-id="f83c3-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="f83c3-128">Az alapértelmezett érték a 3600.</span><span class="sxs-lookup"><span data-stu-id="f83c3-128">Default is 3600.</span></span>

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

### <span data-ttu-id="f83c3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f83c3-129">-InputObject</span></span>
<span data-ttu-id="f83c3-130">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="f83c3-130">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f83c3-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f83c3-131">-IotHubName</span></span>
<span data-ttu-id="f83c3-132">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="f83c3-132">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c3-133">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="f83c3-133">-KeyName</span></span>
<span data-ttu-id="f83c3-134">Az Access-kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="f83c3-134">Access key name.</span></span>

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

### <span data-ttu-id="f83c3-135">-Típus</span><span class="sxs-lookup"><span data-stu-id="f83c3-135">-KeyType</span></span>
<span data-ttu-id="f83c3-136">Az Access-kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="f83c3-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c3-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="f83c3-137">-ModuleId</span></span>
<span data-ttu-id="f83c3-138">A cél modul azonosítója</span><span class="sxs-lookup"><span data-stu-id="f83c3-138">Target Module Id.</span></span>

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

### <span data-ttu-id="f83c3-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83c3-139">-ResourceGroupName</span></span>
<span data-ttu-id="f83c3-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f83c3-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c3-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f83c3-141">-ResourceId</span></span>
<span data-ttu-id="f83c3-142">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f83c3-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83c3-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f83c3-143">-Confirm</span></span>
<span data-ttu-id="f83c3-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f83c3-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83c3-145">-WhatIf</span></span>
<span data-ttu-id="f83c3-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f83c3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f83c3-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f83c3-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83c3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83c3-148">CommonParameters</span></span>
<span data-ttu-id="f83c3-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f83c3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83c3-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f83c3-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83c3-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f83c3-151">INPUTS</span></span>

### <span data-ttu-id="f83c3-152">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f83c3-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f83c3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f83c3-153">System.String</span></span>

## <span data-ttu-id="f83c3-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f83c3-154">OUTPUTS</span></span>

### <span data-ttu-id="f83c3-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f83c3-155">System.String</span></span>

## <span data-ttu-id="f83c3-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f83c3-156">NOTES</span></span>

## <span data-ttu-id="f83c3-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f83c3-157">RELATED LINKS</span></span>
