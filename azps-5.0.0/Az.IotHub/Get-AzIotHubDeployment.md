---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187756"
---
# <span data-ttu-id="2241f-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="2241f-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="2241f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2241f-102">SYNOPSIS</span></span>
<span data-ttu-id="2241f-103">Felsorolja az egész vagy egy adott IoT-alapú központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="2241f-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="2241f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2241f-104">SYNTAX</span></span>

### <span data-ttu-id="2241f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2241f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2241f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2241f-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2241f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2241f-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2241f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2241f-108">DESCRIPTION</span></span>
<span data-ttu-id="2241f-109">Megtudhatja, hogy miként IoT meg a IoT Edge-példányok központi telepítését egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="2241f-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="2241f-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="2241f-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="2241f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2241f-111">EXAMPLES</span></span>

### <span data-ttu-id="2241f-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2241f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="2241f-113">Megtudhatja, hogy miként veheti fel a IoT Edge-példányát.</span><span class="sxs-lookup"><span data-stu-id="2241f-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="2241f-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="2241f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="2241f-115">Felsorolja az összes IoT Edge-példányát egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="2241f-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="2241f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2241f-116">PARAMETERS</span></span>

### <span data-ttu-id="2241f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2241f-117">-DefaultProfile</span></span>
<span data-ttu-id="2241f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2241f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2241f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2241f-119">-InputObject</span></span>
<span data-ttu-id="2241f-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="2241f-120">IotHub object</span></span>

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

### <span data-ttu-id="2241f-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2241f-121">-IotHubName</span></span>
<span data-ttu-id="2241f-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="2241f-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2241f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2241f-123">-Name</span></span>
<span data-ttu-id="2241f-124">A központi telepítő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2241f-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="2241f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2241f-125">-ResourceGroupName</span></span>
<span data-ttu-id="2241f-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2241f-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2241f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2241f-127">-ResourceId</span></span>
<span data-ttu-id="2241f-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="2241f-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2241f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2241f-129">CommonParameters</span></span>
<span data-ttu-id="2241f-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2241f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2241f-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2241f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2241f-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2241f-132">INPUTS</span></span>

### <span data-ttu-id="2241f-133">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2241f-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2241f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2241f-134">System.String</span></span>

## <span data-ttu-id="2241f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2241f-135">OUTPUTS</span></span>

### <span data-ttu-id="2241f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2241f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="2241f-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="2241f-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="2241f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2241f-138">NOTES</span></span>

## <span data-ttu-id="2241f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2241f-139">RELATED LINKS</span></span>
