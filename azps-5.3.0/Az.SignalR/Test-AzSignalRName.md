---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468525"
---
# <span data-ttu-id="0df08-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="0df08-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="0df08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df08-102">SYNOPSIS</span></span>
<span data-ttu-id="0df08-103">Ellenőrizze egy név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="0df08-103">Check the availability of a name.</span></span> <span data-ttu-id="0df08-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="0df08-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="0df08-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0df08-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0df08-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0df08-106">DESCRIPTION</span></span>
<span data-ttu-id="0df08-107">Ellenőrizze egy név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="0df08-107">Check the availability of a name.</span></span> <span data-ttu-id="0df08-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="0df08-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="0df08-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0df08-109">EXAMPLES</span></span>

### <span data-ttu-id="0df08-110">Létező név ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="0df08-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="0df08-111">Ellenőrizze a nem éklött nevet.</span><span class="sxs-lookup"><span data-stu-id="0df08-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="0df08-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0df08-112">PARAMETERS</span></span>

### <span data-ttu-id="0df08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df08-113">-DefaultProfile</span></span>
<span data-ttu-id="0df08-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0df08-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0df08-115">-Location</span><span class="sxs-lookup"><span data-stu-id="0df08-115">-Location</span></span>
<span data-ttu-id="0df08-116">A SignalR szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="0df08-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="0df08-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0df08-117">-Name</span></span>
<span data-ttu-id="0df08-118">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0df08-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="0df08-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df08-119">CommonParameters</span></span>
<span data-ttu-id="0df08-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df08-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df08-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0df08-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df08-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0df08-122">INPUTS</span></span>

### <span data-ttu-id="0df08-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0df08-123">System.String</span></span>

## <span data-ttu-id="0df08-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0df08-124">OUTPUTS</span></span>

### <span data-ttu-id="0df08-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0df08-125">System.Boolean</span></span>

## <span data-ttu-id="0df08-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0df08-126">NOTES</span></span>

## <span data-ttu-id="0df08-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0df08-127">RELATED LINKS</span></span>
