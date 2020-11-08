---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011283"
---
# <span data-ttu-id="3c525-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="3c525-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="3c525-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c525-102">SYNOPSIS</span></span>
<span data-ttu-id="3c525-103">Ellenőrizze a név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="3c525-103">Check the availability of a name.</span></span> <span data-ttu-id="3c525-104">Alias: teszt-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="3c525-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="3c525-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c525-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c525-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c525-106">DESCRIPTION</span></span>
<span data-ttu-id="3c525-107">Ellenőrizze a név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="3c525-107">Check the availability of a name.</span></span> <span data-ttu-id="3c525-108">Alias: teszt-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="3c525-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="3c525-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3c525-109">EXAMPLES</span></span>

### <span data-ttu-id="3c525-110">Ellenőrizze a létező nevet.</span><span class="sxs-lookup"><span data-stu-id="3c525-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="3c525-111">Ellenőrizze a nem létező nevet.</span><span class="sxs-lookup"><span data-stu-id="3c525-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="3c525-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c525-112">PARAMETERS</span></span>

### <span data-ttu-id="3c525-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c525-113">-DefaultProfile</span></span>
<span data-ttu-id="3c525-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c525-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c525-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="3c525-115">-Location</span></span>
<span data-ttu-id="3c525-116">A jelző szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="3c525-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="3c525-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c525-117">-Name</span></span>
<span data-ttu-id="3c525-118">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="3c525-118">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c525-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c525-119">CommonParameters</span></span>
<span data-ttu-id="3c525-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c525-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c525-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c525-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c525-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c525-122">INPUTS</span></span>

### <span data-ttu-id="3c525-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3c525-123">System.String</span></span>

## <span data-ttu-id="3c525-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c525-124">OUTPUTS</span></span>

### <span data-ttu-id="3c525-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c525-125">System.Boolean</span></span>

## <span data-ttu-id="3c525-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c525-126">NOTES</span></span>

## <span data-ttu-id="3c525-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c525-127">RELATED LINKS</span></span>
