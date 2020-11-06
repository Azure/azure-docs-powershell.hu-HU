---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497356"
---
# <span data-ttu-id="c46ee-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c46ee-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="c46ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c46ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c46ee-103">A fiók API-kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="c46ee-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="c46ee-104">Ezek a kulcsok az Azure Maps további hívásokban használt hitelesítési mechanizmusát jelentik.</span><span class="sxs-lookup"><span data-stu-id="c46ee-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c46ee-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c46ee-105">SYNTAX</span></span>

### <span data-ttu-id="c46ee-106">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c46ee-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c46ee-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46ee-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c46ee-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46ee-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c46ee-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c46ee-109">DESCRIPTION</span></span>
<span data-ttu-id="c46ee-110">A Get-AzureRmMapsAccountKey parancsmag a kiépített Azure Maps-fiók API-kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c46ee-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="c46ee-111">Az Azure Maps-fiók két API-kulcsból áll: elsődleges és másodlagos.</span><span class="sxs-lookup"><span data-stu-id="c46ee-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="c46ee-112">A billentyűk lehetővé teszik az Azure Maps-fiók végpontjának interakcióját.</span><span class="sxs-lookup"><span data-stu-id="c46ee-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="c46ee-113">A billentyűk újragenerálásához használja a New-AzureRmMapsAccountKey (új-AzureRmMapsAccountKey. MD) parancsot.</span><span class="sxs-lookup"><span data-stu-id="c46ee-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="c46ee-114">Példák</span><span class="sxs-lookup"><span data-stu-id="c46ee-114">EXAMPLES</span></span>

### <span data-ttu-id="c46ee-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c46ee-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="c46ee-116">A MyAccount nevű fiók kulcsait számítja ki az erőforráscsoport MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c46ee-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c46ee-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="c46ee-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="c46ee-118">A megadott Azure Maps-fiók kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c46ee-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="c46ee-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c46ee-119">PARAMETERS</span></span>

### <span data-ttu-id="c46ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46ee-120">-DefaultProfile</span></span>
<span data-ttu-id="c46ee-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c46ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c46ee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c46ee-122">-InputObject</span></span>
<span data-ttu-id="c46ee-123">A Get-AzureRmMapsAccount átirányítja a fiókját.</span><span class="sxs-lookup"><span data-stu-id="c46ee-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c46ee-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c46ee-124">-Name</span></span>
<span data-ttu-id="c46ee-125">A fiók nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="c46ee-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c46ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="c46ee-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c46ee-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c46ee-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c46ee-128">-ResourceId</span></span>
<span data-ttu-id="c46ee-129">Térképek fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c46ee-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c46ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46ee-130">CommonParameters</span></span>
<span data-ttu-id="c46ee-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c46ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46ee-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c46ee-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46ee-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c46ee-133">INPUTS</span></span>

### <span data-ttu-id="c46ee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c46ee-134">System.String</span></span>

### <span data-ttu-id="c46ee-135">Microsoft. Azure. commands. maps. models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c46ee-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="c46ee-136">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c46ee-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c46ee-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c46ee-137">OUTPUTS</span></span>

### <span data-ttu-id="c46ee-138">Microsoft. Azure. commands. maps. models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c46ee-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="c46ee-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c46ee-139">NOTES</span></span>

## <span data-ttu-id="c46ee-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c46ee-140">RELATED LINKS</span></span>
