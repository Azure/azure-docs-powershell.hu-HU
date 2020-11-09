---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302384"
---
# <span data-ttu-id="0fb32-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="0fb32-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="0fb32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fb32-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb32-103">Ellenőrizze a név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="0fb32-103">Check the availability of a name.</span></span> <span data-ttu-id="0fb32-104">Alias: teszt-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="0fb32-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="0fb32-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fb32-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fb32-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fb32-106">DESCRIPTION</span></span>
<span data-ttu-id="0fb32-107">Ellenőrizze a név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="0fb32-107">Check the availability of a name.</span></span> <span data-ttu-id="0fb32-108">Alias: teszt-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="0fb32-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="0fb32-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0fb32-109">EXAMPLES</span></span>

### <span data-ttu-id="0fb32-110">Ellenőrizze a létező nevet.</span><span class="sxs-lookup"><span data-stu-id="0fb32-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="0fb32-111">Ellenőrizze a nem létező nevet.</span><span class="sxs-lookup"><span data-stu-id="0fb32-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="0fb32-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fb32-112">PARAMETERS</span></span>

### <span data-ttu-id="0fb32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb32-113">-DefaultProfile</span></span>
<span data-ttu-id="0fb32-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fb32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fb32-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="0fb32-115">-Location</span></span>
<span data-ttu-id="0fb32-116">A jelző szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="0fb32-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="0fb32-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fb32-117">-Name</span></span>
<span data-ttu-id="0fb32-118">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0fb32-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="0fb32-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb32-119">CommonParameters</span></span>
<span data-ttu-id="0fb32-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fb32-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb32-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fb32-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb32-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fb32-122">INPUTS</span></span>

### <span data-ttu-id="0fb32-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0fb32-123">System.String</span></span>

## <span data-ttu-id="0fb32-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fb32-124">OUTPUTS</span></span>

### <span data-ttu-id="0fb32-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fb32-125">System.Boolean</span></span>

## <span data-ttu-id="0fb32-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fb32-126">NOTES</span></span>

## <span data-ttu-id="0fb32-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fb32-127">RELATED LINKS</span></span>
