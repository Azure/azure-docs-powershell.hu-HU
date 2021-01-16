---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329994"
---
# <span data-ttu-id="19c0d-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="19c0d-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="19c0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="19c0d-103">Felsorolja az összes vagy egy adott IoT Edge-telepítést.</span><span class="sxs-lookup"><span data-stu-id="19c0d-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="19c0d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19c0d-104">SYNTAX</span></span>

### <span data-ttu-id="19c0d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19c0d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c0d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="19c0d-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19c0d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="19c0d-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19c0d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19c0d-108">DESCRIPTION</span></span>
<span data-ttu-id="19c0d-109">Az IoT Edge-telepítés vagy az IoT Edge-telepítések listája az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="19c0d-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="19c0d-110">További https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="19c0d-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="19c0d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19c0d-111">EXAMPLES</span></span>

### <span data-ttu-id="19c0d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="19c0d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="19c0d-113">Az IoT Edge-telepítés részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="19c0d-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="19c0d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="19c0d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="19c0d-115">Az IoT-központban felsorolja az Összes IoT Edge-telepítést.</span><span class="sxs-lookup"><span data-stu-id="19c0d-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="19c0d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19c0d-116">PARAMETERS</span></span>

### <span data-ttu-id="19c0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c0d-117">-DefaultProfile</span></span>
<span data-ttu-id="19c0d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19c0d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c0d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19c0d-119">-InputObject</span></span>
<span data-ttu-id="19c0d-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="19c0d-120">IotHub object</span></span>

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

### <span data-ttu-id="19c0d-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="19c0d-121">-IotHubName</span></span>
<span data-ttu-id="19c0d-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="19c0d-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="19c0d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="19c0d-123">-Name</span></span>
<span data-ttu-id="19c0d-124">A központi telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="19c0d-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="19c0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="19c0d-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="19c0d-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="19c0d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19c0d-127">-ResourceId</span></span>
<span data-ttu-id="19c0d-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="19c0d-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="19c0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c0d-129">CommonParameters</span></span>
<span data-ttu-id="19c0d-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c0d-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c0d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c0d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19c0d-132">INPUTS</span></span>

### <span data-ttu-id="19c0d-133">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="19c0d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="19c0d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="19c0d-134">System.String</span></span>

## <span data-ttu-id="19c0d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19c0d-135">OUTPUTS</span></span>

### <span data-ttu-id="19c0d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="19c0d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="19c0d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span><span class="sxs-lookup"><span data-stu-id="19c0d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="19c0d-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19c0d-138">NOTES</span></span>

## <span data-ttu-id="19c0d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19c0d-139">RELATED LINKS</span></span>
