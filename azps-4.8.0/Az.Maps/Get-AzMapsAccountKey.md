---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024731"
---
# <span data-ttu-id="c2abc-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c2abc-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="c2abc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2abc-102">SYNOPSIS</span></span>
<span data-ttu-id="c2abc-103">A fiók API-kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="c2abc-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="c2abc-104">Ezek a kulcsok az Azure Maps további hívásokban használt hitelesítési mechanizmusát jelentik.</span><span class="sxs-lookup"><span data-stu-id="c2abc-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="c2abc-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2abc-105">SYNTAX</span></span>

### <span data-ttu-id="c2abc-106">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2abc-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2abc-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2abc-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2abc-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2abc-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2abc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2abc-109">DESCRIPTION</span></span>
<span data-ttu-id="c2abc-110">A Get-AzMapsAccountKey parancsmag a kiépített Azure Maps-fiók API-kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c2abc-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="c2abc-111">Az Azure Maps-fiók két API-kulcsból áll: elsődleges és másodlagos.</span><span class="sxs-lookup"><span data-stu-id="c2abc-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="c2abc-112">A billentyűk lehetővé teszik az Azure Maps-fiók végpontjának interakcióját.</span><span class="sxs-lookup"><span data-stu-id="c2abc-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="c2abc-113">A billentyűk újragenerálásához használja a New-AzMapsAccountKey (új-AzMapsAccountKey. MD) parancsot.</span><span class="sxs-lookup"><span data-stu-id="c2abc-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="c2abc-114">Példák</span><span class="sxs-lookup"><span data-stu-id="c2abc-114">EXAMPLES</span></span>

### <span data-ttu-id="c2abc-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c2abc-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="c2abc-116">A MyAccount nevű fiók kulcsait számítja ki az erőforráscsoport MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c2abc-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c2abc-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="c2abc-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="c2abc-118">A megadott Azure Maps-fiók kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c2abc-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="c2abc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2abc-119">PARAMETERS</span></span>

### <span data-ttu-id="c2abc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2abc-120">-DefaultProfile</span></span>
<span data-ttu-id="c2abc-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2abc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2abc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2abc-122">-InputObject</span></span>
<span data-ttu-id="c2abc-123">A Get-AzMapsAccount átirányítja a fiókját.</span><span class="sxs-lookup"><span data-stu-id="c2abc-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="c2abc-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2abc-124">-Name</span></span>
<span data-ttu-id="c2abc-125">A fiók nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="c2abc-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="c2abc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2abc-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2abc-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c2abc-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2abc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2abc-128">-ResourceId</span></span>
<span data-ttu-id="c2abc-129">Térképek fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c2abc-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="c2abc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2abc-130">CommonParameters</span></span>
<span data-ttu-id="c2abc-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2abc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2abc-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2abc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2abc-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2abc-133">INPUTS</span></span>

### <span data-ttu-id="c2abc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c2abc-134">System.String</span></span>

### <span data-ttu-id="c2abc-135">Microsoft. Azure. commands. maps. models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c2abc-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="c2abc-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2abc-136">OUTPUTS</span></span>

### <span data-ttu-id="c2abc-137">Microsoft. Azure. commands. maps. models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c2abc-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="c2abc-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2abc-138">NOTES</span></span>

## <span data-ttu-id="c2abc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2abc-139">RELATED LINKS</span></span>
