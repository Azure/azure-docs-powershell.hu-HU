---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: 33232e5e8f415309bec36f8918c272c251835f82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503664"
---
# <span data-ttu-id="1efef-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="1efef-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="1efef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1efef-102">SYNOPSIS</span></span>
<span data-ttu-id="1efef-103">Kap egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="1efef-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1efef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1efef-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1efef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1efef-105">DESCRIPTION</span></span>
<span data-ttu-id="1efef-106">Kap egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="1efef-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="1efef-107">Az összes billentyűt felsorolhatja, vagy egy adott kulcsnév alapján szűrheti a listát.</span><span class="sxs-lookup"><span data-stu-id="1efef-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="1efef-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1efef-108">EXAMPLES</span></span>

### <span data-ttu-id="1efef-109">Példa 1 minden billentyű lekérése</span><span class="sxs-lookup"><span data-stu-id="1efef-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1efef-110">A "myiothub" nevű IotHub összes kulcsát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1efef-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="1efef-111">2. példa adott kulcs adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="1efef-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="1efef-112">A "myiothub" nevű IotHub "iothubowner" nevű kulcsához tartozó információkat kapja.</span><span class="sxs-lookup"><span data-stu-id="1efef-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="1efef-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1efef-113">PARAMETERS</span></span>

### <span data-ttu-id="1efef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1efef-114">-DefaultProfile</span></span>
<span data-ttu-id="1efef-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1efef-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1efef-116">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="1efef-116">-KeyName</span></span>
<span data-ttu-id="1efef-117">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="1efef-117">Name of the Key</span></span>

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

### <span data-ttu-id="1efef-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1efef-118">-Name</span></span>
<span data-ttu-id="1efef-119">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="1efef-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="1efef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1efef-120">-ResourceGroupName</span></span>
<span data-ttu-id="1efef-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1efef-121">Resource Group Name</span></span>

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

### <span data-ttu-id="1efef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efef-122">CommonParameters</span></span>
<span data-ttu-id="1efef-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1efef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efef-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1efef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efef-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1efef-125">INPUTS</span></span>

### <span data-ttu-id="1efef-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1efef-126">System.String</span></span>

## <span data-ttu-id="1efef-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1efef-127">OUTPUTS</span></span>

### <span data-ttu-id="1efef-128">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1efef-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="1efef-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1efef-129">NOTES</span></span>

## <span data-ttu-id="1efef-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1efef-130">RELATED LINKS</span></span>
