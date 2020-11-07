---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: ac56d5392025a85d0310862a1786dde3d0f8ca2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835890"
---
# <span data-ttu-id="e35e2-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e35e2-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="e35e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e35e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e35e2-103">Kap egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="e35e2-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="e35e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e35e2-104">SYNTAX</span></span>

```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e35e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e35e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e35e2-106">Kap egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="e35e2-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="e35e2-107">Az összes billentyűt felsorolhatja, vagy egy adott kulcsnév alapján szűrheti a listát.</span><span class="sxs-lookup"><span data-stu-id="e35e2-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="e35e2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e35e2-108">EXAMPLES</span></span>

### <span data-ttu-id="e35e2-109">Példa 1 minden billentyű lekérése</span><span class="sxs-lookup"><span data-stu-id="e35e2-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e35e2-110">A "myiothub" nevű IotHub összes kulcsát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e35e2-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="e35e2-111">2. példa adott kulcs adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e35e2-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="e35e2-112">A "myiothub" nevű IotHub "iothubowner" nevű kulcsához tartozó információkat kapja.</span><span class="sxs-lookup"><span data-stu-id="e35e2-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e35e2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e35e2-113">PARAMETERS</span></span>

### <span data-ttu-id="e35e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35e2-114">-DefaultProfile</span></span>
<span data-ttu-id="e35e2-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e35e2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e35e2-116">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="e35e2-116">-KeyName</span></span>
<span data-ttu-id="e35e2-117">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="e35e2-117">Name of the Key</span></span>

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

### <span data-ttu-id="e35e2-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e35e2-118">-Name</span></span>
<span data-ttu-id="e35e2-119">A IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="e35e2-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="e35e2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35e2-120">-ResourceGroupName</span></span>
<span data-ttu-id="e35e2-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e35e2-121">Resource Group Name</span></span>

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

### <span data-ttu-id="e35e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35e2-122">CommonParameters</span></span>
<span data-ttu-id="e35e2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e35e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35e2-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35e2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35e2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e35e2-125">INPUTS</span></span>

### <span data-ttu-id="e35e2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e35e2-126">System.String</span></span>

## <span data-ttu-id="e35e2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e35e2-127">OUTPUTS</span></span>

### <span data-ttu-id="e35e2-128">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e35e2-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e35e2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e35e2-129">NOTES</span></span>

## <span data-ttu-id="e35e2-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e35e2-130">RELATED LINKS</span></span>
