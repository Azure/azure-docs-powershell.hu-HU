---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 21fbee422b898b5e5cf448f4a8f1913777268964
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837978"
---
# <span data-ttu-id="4efff-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="4efff-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="4efff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4efff-102">SYNOPSIS</span></span>
<span data-ttu-id="4efff-103">Ellenőrizze a név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="4efff-103">Check the availability of a name.</span></span> <span data-ttu-id="4efff-104">Alias: teszt-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="4efff-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="4efff-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4efff-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4efff-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="4efff-106">DESCRIPTION</span></span>
<span data-ttu-id="4efff-107">Ellenőrizze a név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="4efff-107">Check the availability of a name.</span></span> <span data-ttu-id="4efff-108">Alias: teszt-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="4efff-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="4efff-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4efff-109">EXAMPLES</span></span>

### <span data-ttu-id="4efff-110">Ellenőrizze a létező nevet.</span><span class="sxs-lookup"><span data-stu-id="4efff-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="4efff-111">Ellenőrizze a nem létező nevet.</span><span class="sxs-lookup"><span data-stu-id="4efff-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="4efff-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4efff-112">PARAMETERS</span></span>

### <span data-ttu-id="4efff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efff-113">-DefaultProfile</span></span>
<span data-ttu-id="4efff-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4efff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4efff-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="4efff-115">-Location</span></span>
<span data-ttu-id="4efff-116">A jelző szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="4efff-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="4efff-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4efff-117">-Name</span></span>
<span data-ttu-id="4efff-118">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="4efff-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="4efff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efff-119">CommonParameters</span></span>
<span data-ttu-id="4efff-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4efff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efff-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4efff-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efff-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4efff-122">INPUTS</span></span>

### <span data-ttu-id="4efff-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4efff-123">System.String</span></span>

## <span data-ttu-id="4efff-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4efff-124">OUTPUTS</span></span>

### <span data-ttu-id="4efff-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4efff-125">System.Boolean</span></span>

## <span data-ttu-id="4efff-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4efff-126">NOTES</span></span>

## <span data-ttu-id="4efff-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4efff-127">RELATED LINKS</span></span>
