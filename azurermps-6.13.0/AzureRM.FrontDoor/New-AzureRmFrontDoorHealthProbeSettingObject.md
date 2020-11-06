---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496179"
---
# <span data-ttu-id="d4abe-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="d4abe-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="d4abe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4abe-102">SYNOPSIS</span></span>
<span data-ttu-id="d4abe-103">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="d4abe-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4abe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4abe-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4abe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4abe-105">DESCRIPTION</span></span>
<span data-ttu-id="d4abe-106">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="d4abe-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="d4abe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d4abe-107">EXAMPLES</span></span>

### <span data-ttu-id="d4abe-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4abe-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="d4abe-109">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="d4abe-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="d4abe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4abe-110">PARAMETERS</span></span>

### <span data-ttu-id="d4abe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4abe-111">-DefaultProfile</span></span>
<span data-ttu-id="d4abe-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4abe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4abe-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d4abe-113">-IntervalInSeconds</span></span>
<span data-ttu-id="d4abe-114">Az egészségügyi Szondák közötti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="d4abe-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="d4abe-115">Az alapértelmezett érték 30</span><span class="sxs-lookup"><span data-stu-id="d4abe-115">Default value is 30</span></span>

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

### <span data-ttu-id="d4abe-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4abe-116">-Name</span></span>
<span data-ttu-id="d4abe-117">az állapot-szonda beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="d4abe-117">health probe setting name.</span></span>

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

### <span data-ttu-id="d4abe-118">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d4abe-118">-Path</span></span>
<span data-ttu-id="d4abe-119">Az állapot-szonda használati útvonala.</span><span class="sxs-lookup"><span data-stu-id="d4abe-119">The path to use for the health probe.</span></span>
<span data-ttu-id="d4abe-120">Alapértelmezett érték/</span><span class="sxs-lookup"><span data-stu-id="d4abe-120">Default is /</span></span>

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

### <span data-ttu-id="d4abe-121">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d4abe-121">-Protocol</span></span>
<span data-ttu-id="d4abe-122">Az ehhez a szonda alapértelmezett értékéhez használandó Protocol-séma HTTP</span><span class="sxs-lookup"><span data-stu-id="d4abe-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="d4abe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4abe-123">CommonParameters</span></span>
<span data-ttu-id="d4abe-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4abe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4abe-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4abe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4abe-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4abe-126">INPUTS</span></span>

### <span data-ttu-id="d4abe-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="d4abe-127">None</span></span>

## <span data-ttu-id="d4abe-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4abe-128">OUTPUTS</span></span>

### <span data-ttu-id="d4abe-129">Microsoft. Azure. Command. FrontDoor. models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="d4abe-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="d4abe-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4abe-130">NOTES</span></span>

## <span data-ttu-id="d4abe-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4abe-131">RELATED LINKS</span></span>

<span data-ttu-id="d4abe-132">[Új – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d4abe-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
