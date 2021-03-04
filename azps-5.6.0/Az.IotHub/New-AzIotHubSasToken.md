---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 39b936f6b9ec4bb133ecc6510963207c5e7d96a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931137"
---
# <span data-ttu-id="def2f-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="def2f-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="def2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="def2f-102">SYNOPSIS</span></span>
<span data-ttu-id="def2f-103">Egy célként megadott IoT-központhoz, eszközhöz vagy modulhoz hozzon létre EGY SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="def2f-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="def2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="def2f-104">SYNTAX</span></span>

### <span data-ttu-id="def2f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="def2f-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def2f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="def2f-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="def2f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="def2f-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="def2f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="def2f-108">DESCRIPTION</span></span>
<span data-ttu-id="def2f-109">Az eszköz SAS-jogkivonatai esetén a házirend paramétere csak az eszköz beállításjegyzékének eléréséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="def2f-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="def2f-110">Ezért a házirendnek olvasási hozzáféréssel kell lennie a beállításjegyzékhez.</span><span class="sxs-lookup"><span data-stu-id="def2f-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="def2f-111">Az IoT-központ jogkivonatainál a házirend az SAS részét képezi.</span><span class="sxs-lookup"><span data-stu-id="def2f-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="def2f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="def2f-112">EXAMPLES</span></span>

### <span data-ttu-id="def2f-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="def2f-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="def2f-114">Hozzon létre egy IoT Hub SAS-jogkivonatot az iothubowner házirend és az elsődleges kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="def2f-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="def2f-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="def2f-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="def2f-116">Hozzon létre egy IoT Hub SAS-jogkivonatot a registryRead házirend és a másodlagos kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="def2f-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="def2f-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="def2f-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="def2f-118">Hozzon létre egy eszköz SAS-jogkivonatot az iothubowner házirend használatával a(z) {iothub_name} eszköz beállításjegyzékének eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="def2f-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="def2f-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="def2f-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="def2f-120">Hozzon létre egy MODUL SAS-jogkivonatot az iothubowner házirend használatával a(z) {iothub_name} eszköz beállításjegyzékének eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="def2f-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="def2f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="def2f-121">PARAMETERS</span></span>

### <span data-ttu-id="def2f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def2f-122">-DefaultProfile</span></span>
<span data-ttu-id="def2f-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="def2f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="def2f-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="def2f-124">-DeviceId</span></span>
<span data-ttu-id="def2f-125">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="def2f-125">Target Device Id.</span></span>

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

### <span data-ttu-id="def2f-126">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="def2f-126">-Duration</span></span>
<span data-ttu-id="def2f-127">A jövőbeli érvényesség (másodpercben) lejár a létrehozendő jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="def2f-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="def2f-128">Az alapértelmezett érték 3600.</span><span class="sxs-lookup"><span data-stu-id="def2f-128">Default is 3600.</span></span>

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

### <span data-ttu-id="def2f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="def2f-129">-InputObject</span></span>
<span data-ttu-id="def2f-130">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="def2f-130">IotHub object</span></span>

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

### <span data-ttu-id="def2f-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="def2f-131">-IotHubName</span></span>
<span data-ttu-id="def2f-132">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="def2f-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="def2f-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="def2f-133">-KeyName</span></span>
<span data-ttu-id="def2f-134">Access-kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="def2f-134">Access key name.</span></span>

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

### <span data-ttu-id="def2f-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="def2f-135">-KeyType</span></span>
<span data-ttu-id="def2f-136">Az Access billentyűtípusa.</span><span class="sxs-lookup"><span data-stu-id="def2f-136">Access key type.</span></span>

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

### <span data-ttu-id="def2f-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="def2f-137">-ModuleId</span></span>
<span data-ttu-id="def2f-138">Célmodul-azonosító.</span><span class="sxs-lookup"><span data-stu-id="def2f-138">Target Module Id.</span></span>

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

### <span data-ttu-id="def2f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def2f-139">-ResourceGroupName</span></span>
<span data-ttu-id="def2f-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="def2f-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="def2f-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="def2f-141">-ResourceId</span></span>
<span data-ttu-id="def2f-142">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="def2f-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="def2f-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="def2f-143">-Confirm</span></span>
<span data-ttu-id="def2f-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="def2f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="def2f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def2f-145">-WhatIf</span></span>
<span data-ttu-id="def2f-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="def2f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def2f-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="def2f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="def2f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def2f-148">CommonParameters</span></span>
<span data-ttu-id="def2f-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def2f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def2f-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def2f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def2f-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="def2f-151">INPUTS</span></span>

### <span data-ttu-id="def2f-152">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="def2f-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="def2f-153">System.String</span><span class="sxs-lookup"><span data-stu-id="def2f-153">System.String</span></span>

## <span data-ttu-id="def2f-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="def2f-154">OUTPUTS</span></span>

### <span data-ttu-id="def2f-155">System.String</span><span class="sxs-lookup"><span data-stu-id="def2f-155">System.String</span></span>

## <span data-ttu-id="def2f-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="def2f-156">NOTES</span></span>

## <span data-ttu-id="def2f-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="def2f-157">RELATED LINKS</span></span>
