---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329970"
---
# <span data-ttu-id="66535-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="66535-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="66535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66535-102">SYNOPSIS</span></span>
<span data-ttu-id="66535-103">Eszközeszközt kap.</span><span class="sxs-lookup"><span data-stu-id="66535-103">Gets a device twin.</span></span>

## <span data-ttu-id="66535-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66535-104">SYNTAX</span></span>

### <span data-ttu-id="66535-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66535-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66535-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66535-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66535-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="66535-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66535-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66535-108">DESCRIPTION</span></span>
<span data-ttu-id="66535-109">Eszközeszközt kap.</span><span class="sxs-lookup"><span data-stu-id="66535-109">Gets a device twin.</span></span> <span data-ttu-id="66535-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="66535-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="66535-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66535-111">EXAMPLES</span></span>

### <span data-ttu-id="66535-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="66535-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="66535-113">Az eszköz objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="66535-113">Returns the device twin object.</span></span>

## <span data-ttu-id="66535-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66535-114">PARAMETERS</span></span>

### <span data-ttu-id="66535-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66535-115">-DefaultProfile</span></span>
<span data-ttu-id="66535-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66535-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66535-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="66535-117">-DeviceId</span></span>
<span data-ttu-id="66535-118">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66535-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66535-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66535-119">-InputObject</span></span>
<span data-ttu-id="66535-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="66535-120">IotHub object</span></span>

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

### <span data-ttu-id="66535-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="66535-121">-IotHubName</span></span>
<span data-ttu-id="66535-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="66535-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="66535-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66535-123">-ResourceGroupName</span></span>
<span data-ttu-id="66535-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="66535-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="66535-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66535-125">-ResourceId</span></span>
<span data-ttu-id="66535-126">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="66535-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="66535-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66535-127">CommonParameters</span></span>
<span data-ttu-id="66535-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66535-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66535-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66535-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66535-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66535-130">INPUTS</span></span>

### <span data-ttu-id="66535-131">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="66535-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="66535-132">System.String</span><span class="sxs-lookup"><span data-stu-id="66535-132">System.String</span></span>

## <span data-ttu-id="66535-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66535-133">OUTPUTS</span></span>

### <span data-ttu-id="66535-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="66535-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="66535-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66535-135">NOTES</span></span>

## <span data-ttu-id="66535-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66535-136">RELATED LINKS</span></span>
