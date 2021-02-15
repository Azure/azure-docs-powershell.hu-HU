---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152923"
---
# <span data-ttu-id="9cb20-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="9cb20-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="9cb20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb20-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb20-103">IotHub-kulcsot kap.</span><span class="sxs-lookup"><span data-stu-id="9cb20-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="9cb20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9cb20-104">SYNTAX</span></span>

### <span data-ttu-id="9cb20-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cb20-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cb20-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9cb20-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cb20-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9cb20-107">DESCRIPTION</span></span>
<span data-ttu-id="9cb20-108">IotHub-kulcsot kap.</span><span class="sxs-lookup"><span data-stu-id="9cb20-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="9cb20-109">Az összes billentyűt listába sorolhatja, vagy adott kulcsnév szerint szűrheti a listát.</span><span class="sxs-lookup"><span data-stu-id="9cb20-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="9cb20-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9cb20-110">EXAMPLES</span></span>

### <span data-ttu-id="9cb20-111">1. példa az összes kulcs be szereznie</span><span class="sxs-lookup"><span data-stu-id="9cb20-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9cb20-112">A myiothub nevű IotHub összes kulcsát beveszi</span><span class="sxs-lookup"><span data-stu-id="9cb20-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="9cb20-113">2. példa adott kulcsra vonatkozó információk lekérte</span><span class="sxs-lookup"><span data-stu-id="9cb20-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="9cb20-114">A "myiothub" nevű IotHub kulcsának "iothubowner" adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="9cb20-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9cb20-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cb20-115">PARAMETERS</span></span>

### <span data-ttu-id="9cb20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb20-116">-DefaultProfile</span></span>
<span data-ttu-id="9cb20-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9cb20-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cb20-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="9cb20-118">-HubId</span></span>
<span data-ttu-id="9cb20-119">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="9cb20-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9cb20-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9cb20-120">-KeyName</span></span>
<span data-ttu-id="9cb20-121">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="9cb20-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb20-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9cb20-122">-Name</span></span>
<span data-ttu-id="9cb20-123">Az IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="9cb20-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb20-124">-ResourceGroupName</span></span>
<span data-ttu-id="9cb20-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9cb20-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb20-126">CommonParameters</span></span>
<span data-ttu-id="9cb20-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb20-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb20-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb20-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cb20-129">INPUTS</span></span>

### <span data-ttu-id="9cb20-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9cb20-130">System.String</span></span>

## <span data-ttu-id="9cb20-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cb20-131">OUTPUTS</span></span>

### <span data-ttu-id="9cb20-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9cb20-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="9cb20-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9cb20-133">NOTES</span></span>

## <span data-ttu-id="9cb20-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cb20-134">RELATED LINKS</span></span>
