---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: db2cf6c9daae5b96642a6408b990276feffc8598
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501828"
---
# <span data-ttu-id="80ba1-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="80ba1-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="80ba1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="80ba1-103">Kap egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="80ba1-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80ba1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80ba1-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80ba1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="80ba1-105">DESCRIPTION</span></span>
<span data-ttu-id="80ba1-106">Kap egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="80ba1-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="80ba1-107">Az összes billentyűt felsorolhatja, vagy egy adott kulcsnév alapján szűrheti a listát.</span><span class="sxs-lookup"><span data-stu-id="80ba1-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="80ba1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="80ba1-108">EXAMPLES</span></span>

### <span data-ttu-id="80ba1-109">Példa 1 minden billentyű lekérése</span><span class="sxs-lookup"><span data-stu-id="80ba1-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="80ba1-110">A "myiothub" nevű IotHub összes kulcsát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80ba1-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="80ba1-111">2. példa adott kulcs adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="80ba1-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="80ba1-112">A "myiothub" nevű IotHub "iothubowner" nevű kulcsához tartozó információkat kapja.</span><span class="sxs-lookup"><span data-stu-id="80ba1-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="80ba1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80ba1-113">PARAMETERS</span></span>

### <span data-ttu-id="80ba1-114">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="80ba1-114">-KeyName</span></span>
<span data-ttu-id="80ba1-115">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="80ba1-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ba1-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80ba1-116">-Name</span></span>
<span data-ttu-id="80ba1-117">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="80ba1-117">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ba1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ba1-118">-ResourceGroupName</span></span>
<span data-ttu-id="80ba1-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="80ba1-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ba1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ba1-120">-DefaultProfile</span></span>
<span data-ttu-id="80ba1-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80ba1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ba1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ba1-122">CommonParameters</span></span>
<span data-ttu-id="80ba1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80ba1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ba1-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80ba1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ba1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80ba1-125">INPUTS</span></span>

### <span data-ttu-id="80ba1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="80ba1-126">System.String</span></span>

## <span data-ttu-id="80ba1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80ba1-127">OUTPUTS</span></span>

### <span data-ttu-id="80ba1-128">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="80ba1-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="80ba1-129">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="80ba1-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="80ba1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80ba1-130">NOTES</span></span>

## <span data-ttu-id="80ba1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80ba1-131">RELATED LINKS</span></span>

