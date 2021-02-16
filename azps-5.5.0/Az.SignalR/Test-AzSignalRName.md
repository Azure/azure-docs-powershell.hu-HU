---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165874"
---
# <span data-ttu-id="efd37-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="efd37-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="efd37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd37-102">SYNOPSIS</span></span>
<span data-ttu-id="efd37-103">Ellenőrizze egy név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="efd37-103">Check the availability of a name.</span></span> <span data-ttu-id="efd37-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="efd37-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="efd37-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efd37-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efd37-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efd37-106">DESCRIPTION</span></span>
<span data-ttu-id="efd37-107">Ellenőrizze egy név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="efd37-107">Check the availability of a name.</span></span> <span data-ttu-id="efd37-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="efd37-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="efd37-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efd37-109">EXAMPLES</span></span>

### <span data-ttu-id="efd37-110">Létező név ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="efd37-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="efd37-111">Ellenőrizze a nem hívták fel a nevére.</span><span class="sxs-lookup"><span data-stu-id="efd37-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="efd37-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efd37-112">PARAMETERS</span></span>

### <span data-ttu-id="efd37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd37-113">-DefaultProfile</span></span>
<span data-ttu-id="efd37-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efd37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efd37-115">-Location</span><span class="sxs-lookup"><span data-stu-id="efd37-115">-Location</span></span>
<span data-ttu-id="efd37-116">A SignalR szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="efd37-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="efd37-117">-Name</span><span class="sxs-lookup"><span data-stu-id="efd37-117">-Name</span></span>
<span data-ttu-id="efd37-118">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="efd37-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="efd37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd37-119">CommonParameters</span></span>
<span data-ttu-id="efd37-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efd37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd37-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efd37-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd37-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efd37-122">INPUTS</span></span>

### <span data-ttu-id="efd37-123">System.String</span><span class="sxs-lookup"><span data-stu-id="efd37-123">System.String</span></span>

## <span data-ttu-id="efd37-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efd37-124">OUTPUTS</span></span>

### <span data-ttu-id="efd37-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efd37-125">System.Boolean</span></span>

## <span data-ttu-id="efd37-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efd37-126">NOTES</span></span>

## <span data-ttu-id="efd37-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efd37-127">RELATED LINKS</span></span>
