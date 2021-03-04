---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 4a63f13e567a5f53726058c831107ce43768c0f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936858"
---
# <span data-ttu-id="ca9a6-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ca9a6-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="ca9a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9a6-103">IotHub-kulcsot kap.</span><span class="sxs-lookup"><span data-stu-id="ca9a6-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="ca9a6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca9a6-104">SYNTAX</span></span>

### <span data-ttu-id="ca9a6-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca9a6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca9a6-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca9a6-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca9a6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca9a6-107">DESCRIPTION</span></span>
<span data-ttu-id="ca9a6-108">IotHub-kulcsot kap.</span><span class="sxs-lookup"><span data-stu-id="ca9a6-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="ca9a6-109">Az összes billentyűt listába sorolhatja, vagy adott kulcsnév szerint szűrheti a listát.</span><span class="sxs-lookup"><span data-stu-id="ca9a6-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="ca9a6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca9a6-110">EXAMPLES</span></span>

### <span data-ttu-id="ca9a6-111">1. példa az összes kulcs be szereznie</span><span class="sxs-lookup"><span data-stu-id="ca9a6-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ca9a6-112">A myiothub nevű IotHub összes kulcsát beveszi</span><span class="sxs-lookup"><span data-stu-id="ca9a6-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="ca9a6-113">2. példa adott kulcsra vonatkozó információk lekérte</span><span class="sxs-lookup"><span data-stu-id="ca9a6-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="ca9a6-114">Az IotHub "myiothub" nevű "iothubowner" kulcsának adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ca9a6-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ca9a6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca9a6-115">PARAMETERS</span></span>

### <span data-ttu-id="ca9a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9a6-116">-DefaultProfile</span></span>
<span data-ttu-id="ca9a6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ca9a6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca9a6-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="ca9a6-118">-HubId</span></span>
<span data-ttu-id="ca9a6-119">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="ca9a6-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ca9a6-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ca9a6-120">-KeyName</span></span>
<span data-ttu-id="ca9a6-121">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="ca9a6-121">Name of the Key</span></span>

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

### <span data-ttu-id="ca9a6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ca9a6-122">-Name</span></span>
<span data-ttu-id="ca9a6-123">Az IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="ca9a6-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="ca9a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca9a6-125">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ca9a6-125">Resource Group Name</span></span>

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

### <span data-ttu-id="ca9a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9a6-126">CommonParameters</span></span>
<span data-ttu-id="ca9a6-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9a6-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9a6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9a6-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca9a6-129">INPUTS</span></span>

### <span data-ttu-id="ca9a6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ca9a6-130">System.String</span></span>

## <span data-ttu-id="ca9a6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca9a6-131">OUTPUTS</span></span>

### <span data-ttu-id="ca9a6-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ca9a6-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="ca9a6-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca9a6-133">NOTES</span></span>

## <span data-ttu-id="ca9a6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca9a6-134">RELATED LINKS</span></span>
