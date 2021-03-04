---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 01fc755564fdfd702773c31a52e13d8a95c40ede
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920297"
---
# <span data-ttu-id="17f4d-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="17f4d-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="17f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="17f4d-103">Ellenőrizze egy név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="17f4d-103">Check the availability of a name.</span></span> <span data-ttu-id="17f4d-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="17f4d-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="17f4d-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17f4d-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17f4d-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17f4d-106">DESCRIPTION</span></span>
<span data-ttu-id="17f4d-107">Ellenőrizze egy név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="17f4d-107">Check the availability of a name.</span></span> <span data-ttu-id="17f4d-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="17f4d-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="17f4d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17f4d-109">EXAMPLES</span></span>

### <span data-ttu-id="17f4d-110">Létező név ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="17f4d-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="17f4d-111">Ellenőrizze a nem éklött nevet.</span><span class="sxs-lookup"><span data-stu-id="17f4d-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="17f4d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17f4d-112">PARAMETERS</span></span>

### <span data-ttu-id="17f4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f4d-113">-DefaultProfile</span></span>
<span data-ttu-id="17f4d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17f4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17f4d-115">-Location</span><span class="sxs-lookup"><span data-stu-id="17f4d-115">-Location</span></span>
<span data-ttu-id="17f4d-116">A SignalR szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="17f4d-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="17f4d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="17f4d-117">-Name</span></span>
<span data-ttu-id="17f4d-118">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="17f4d-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="17f4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f4d-119">CommonParameters</span></span>
<span data-ttu-id="17f4d-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f4d-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17f4d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f4d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17f4d-122">INPUTS</span></span>

### <span data-ttu-id="17f4d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="17f4d-123">System.String</span></span>

## <span data-ttu-id="17f4d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17f4d-124">OUTPUTS</span></span>

### <span data-ttu-id="17f4d-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17f4d-125">System.Boolean</span></span>

## <span data-ttu-id="17f4d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17f4d-126">NOTES</span></span>

## <span data-ttu-id="17f4d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17f4d-127">RELATED LINKS</span></span>
