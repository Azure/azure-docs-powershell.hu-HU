---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666423"
---
# <span data-ttu-id="04e43-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="04e43-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="04e43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04e43-102">SYNOPSIS</span></span>
<span data-ttu-id="04e43-103">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="04e43-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="04e43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04e43-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04e43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04e43-105">DESCRIPTION</span></span>
<span data-ttu-id="04e43-106">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="04e43-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="04e43-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04e43-107">EXAMPLES</span></span>

### <span data-ttu-id="04e43-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="04e43-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="04e43-109">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="04e43-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="04e43-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04e43-110">PARAMETERS</span></span>

### <span data-ttu-id="04e43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e43-111">-DefaultProfile</span></span>
<span data-ttu-id="04e43-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04e43-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04e43-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="04e43-113">-IntervalInSeconds</span></span>
<span data-ttu-id="04e43-114">Az egészségügyi Szondák közötti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="04e43-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="04e43-115">Az alapértelmezett érték 30</span><span class="sxs-lookup"><span data-stu-id="04e43-115">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04e43-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04e43-116">-Name</span></span>
<span data-ttu-id="04e43-117">az állapot-szonda beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="04e43-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04e43-118">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="04e43-118">-Path</span></span>
<span data-ttu-id="04e43-119">Az állapot-szonda használati útvonala.</span><span class="sxs-lookup"><span data-stu-id="04e43-119">The path to use for the health probe.</span></span>
<span data-ttu-id="04e43-120">Alapértelmezett érték/</span><span class="sxs-lookup"><span data-stu-id="04e43-120">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04e43-121">-Protocol</span><span class="sxs-lookup"><span data-stu-id="04e43-121">-Protocol</span></span>
<span data-ttu-id="04e43-122">Az ehhez a szonda alapértelmezett értékéhez használandó Protocol-séma HTTP</span><span class="sxs-lookup"><span data-stu-id="04e43-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04e43-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e43-123">CommonParameters</span></span>
<span data-ttu-id="04e43-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04e43-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e43-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="04e43-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e43-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04e43-126">INPUTS</span></span>

### <span data-ttu-id="04e43-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="04e43-127">None</span></span>

## <span data-ttu-id="04e43-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04e43-128">OUTPUTS</span></span>

### <span data-ttu-id="04e43-129">Microsoft. Azure. Command. FrontDoor. models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="04e43-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="04e43-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04e43-130">NOTES</span></span>

## <span data-ttu-id="04e43-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04e43-131">RELATED LINKS</span></span>

<span data-ttu-id="04e43-132">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="04e43-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
