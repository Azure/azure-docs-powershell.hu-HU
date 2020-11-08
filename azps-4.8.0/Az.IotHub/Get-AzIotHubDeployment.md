---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183558"
---
# <span data-ttu-id="c498c-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="c498c-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="c498c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c498c-102">SYNOPSIS</span></span>
<span data-ttu-id="c498c-103">Felsorolja az egész vagy egy adott IoT-alapú központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="c498c-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="c498c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c498c-104">SYNTAX</span></span>

### <span data-ttu-id="c498c-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c498c-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c498c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c498c-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c498c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c498c-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c498c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c498c-108">DESCRIPTION</span></span>
<span data-ttu-id="c498c-109">Megtudhatja, hogy miként IoT meg a IoT Edge-példányok központi telepítését egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="c498c-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="c498c-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="c498c-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="c498c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c498c-111">EXAMPLES</span></span>

### <span data-ttu-id="c498c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c498c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="c498c-113">Megtudhatja, hogy miként veheti fel a IoT Edge-példányát.</span><span class="sxs-lookup"><span data-stu-id="c498c-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="c498c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c498c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="c498c-115">Felsorolja az összes IoT Edge-példányát egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="c498c-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="c498c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c498c-116">PARAMETERS</span></span>

### <span data-ttu-id="c498c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c498c-117">-DefaultProfile</span></span>
<span data-ttu-id="c498c-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c498c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c498c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c498c-119">-InputObject</span></span>
<span data-ttu-id="c498c-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="c498c-120">IotHub object</span></span>

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

### <span data-ttu-id="c498c-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c498c-121">-IotHubName</span></span>
<span data-ttu-id="c498c-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="c498c-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c498c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c498c-123">-Name</span></span>
<span data-ttu-id="c498c-124">A központi telepítő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c498c-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="c498c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c498c-125">-ResourceGroupName</span></span>
<span data-ttu-id="c498c-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c498c-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c498c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c498c-127">-ResourceId</span></span>
<span data-ttu-id="c498c-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="c498c-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c498c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c498c-129">CommonParameters</span></span>
<span data-ttu-id="c498c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c498c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c498c-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c498c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c498c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c498c-132">INPUTS</span></span>

### <span data-ttu-id="c498c-133">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c498c-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c498c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c498c-134">System.String</span></span>

## <span data-ttu-id="c498c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c498c-135">OUTPUTS</span></span>

### <span data-ttu-id="c498c-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c498c-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="c498c-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="c498c-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="c498c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c498c-138">NOTES</span></span>

## <span data-ttu-id="c498c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c498c-139">RELATED LINKS</span></span>
