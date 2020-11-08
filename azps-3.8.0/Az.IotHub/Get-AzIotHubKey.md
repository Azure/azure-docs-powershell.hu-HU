---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011892"
---
# <span data-ttu-id="f8e04-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="f8e04-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="f8e04-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8e04-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e04-103">Kap egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f8e04-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="f8e04-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8e04-104">SYNTAX</span></span>

### <span data-ttu-id="f8e04-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8e04-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8e04-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f8e04-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8e04-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8e04-107">DESCRIPTION</span></span>
<span data-ttu-id="f8e04-108">Kap egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f8e04-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="f8e04-109">Az összes billentyűt felsorolhatja, vagy egy adott kulcsnév alapján szűrheti a listát.</span><span class="sxs-lookup"><span data-stu-id="f8e04-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="f8e04-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f8e04-110">EXAMPLES</span></span>

### <span data-ttu-id="f8e04-111">Példa 1 minden billentyű lekérése</span><span class="sxs-lookup"><span data-stu-id="f8e04-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f8e04-112">A "myiothub" nevű IotHub összes kulcsát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8e04-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="f8e04-113">2. példa adott kulcs adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="f8e04-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="f8e04-114">A "myiothub" nevű IotHub "iothubowner" nevű kulcsához tartozó információkat kapja.</span><span class="sxs-lookup"><span data-stu-id="f8e04-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f8e04-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8e04-115">PARAMETERS</span></span>

### <span data-ttu-id="f8e04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e04-116">-DefaultProfile</span></span>
<span data-ttu-id="f8e04-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f8e04-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8e04-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="f8e04-118">-HubId</span></span>
<span data-ttu-id="f8e04-119">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f8e04-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f8e04-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="f8e04-120">-KeyName</span></span>
<span data-ttu-id="f8e04-121">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="f8e04-121">Name of the Key</span></span>

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

### <span data-ttu-id="f8e04-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8e04-122">-Name</span></span>
<span data-ttu-id="f8e04-123">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="f8e04-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="f8e04-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e04-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8e04-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f8e04-125">Resource Group Name</span></span>

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

### <span data-ttu-id="f8e04-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e04-126">CommonParameters</span></span>
<span data-ttu-id="f8e04-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8e04-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e04-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e04-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e04-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8e04-129">INPUTS</span></span>

### <span data-ttu-id="f8e04-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f8e04-130">System.String</span></span>

## <span data-ttu-id="f8e04-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8e04-131">OUTPUTS</span></span>

### <span data-ttu-id="f8e04-132">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8e04-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="f8e04-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8e04-133">NOTES</span></span>

## <span data-ttu-id="f8e04-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8e04-134">RELATED LINKS</span></span>
