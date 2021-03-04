---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: bce5110a4aa03686b8ae38ee03ea853bc6c89949
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940417"
---
# <span data-ttu-id="410c4-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="410c4-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="410c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="410c4-102">SYNOPSIS</span></span>
<span data-ttu-id="410c4-103">Egy fiók API-kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="410c4-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="410c4-104">Ezek a kulcsok azok a hitelesítési mechanizmusok, amelyek az Azure Maps későbbi hívása során használatosak.</span><span class="sxs-lookup"><span data-stu-id="410c4-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="410c4-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="410c4-105">SYNTAX</span></span>

### <span data-ttu-id="410c4-106">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="410c4-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="410c4-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="410c4-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="410c4-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="410c4-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="410c4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="410c4-109">DESCRIPTION</span></span>
<span data-ttu-id="410c4-110">A Get-AzMapsAccountKey parancsmag egy kiépített Azure Maps-fiók API-kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="410c4-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="410c4-111">Az Azure Maps-fiók két API-kulcsból áll: Elsődleges és Másodlagos.</span><span class="sxs-lookup"><span data-stu-id="410c4-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="410c4-112">A kulcsok lehetővé teszik az Azure Maps-fiók végpontjának interakcióját.</span><span class="sxs-lookup"><span data-stu-id="410c4-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="410c4-113">A New-AzMapsAccountKey (New-AzMapsAccountKey.md) használatával újragenerál egy kulcsot.</span><span class="sxs-lookup"><span data-stu-id="410c4-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="410c4-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="410c4-114">EXAMPLES</span></span>

### <span data-ttu-id="410c4-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="410c4-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="410c4-116">Visszaadja a MyAccount nevű fiók kulcsait a MyResourceGroup erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="410c4-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="410c4-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="410c4-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="410c4-118">A megadott Azure Maps-fiók kulcsait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="410c4-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="410c4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="410c4-119">PARAMETERS</span></span>

### <span data-ttu-id="410c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410c4-120">-DefaultProfile</span></span>
<span data-ttu-id="410c4-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="410c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="410c4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="410c4-122">-InputObject</span></span>
<span data-ttu-id="410c4-123">Térképek-fiók, amely a Get-AzMapsAccount fájlból van be van pávava.</span><span class="sxs-lookup"><span data-stu-id="410c4-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="410c4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="410c4-124">-Name</span></span>
<span data-ttu-id="410c4-125">Térképek-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="410c4-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="410c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="410c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="410c4-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="410c4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="410c4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="410c4-128">-ResourceId</span></span>
<span data-ttu-id="410c4-129">Leképezi a Fiók erőforrásazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="410c4-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="410c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410c4-130">CommonParameters</span></span>
<span data-ttu-id="410c4-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="410c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410c4-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="410c4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410c4-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="410c4-133">INPUTS</span></span>

### <span data-ttu-id="410c4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="410c4-134">System.String</span></span>

### <span data-ttu-id="410c4-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="410c4-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="410c4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="410c4-136">OUTPUTS</span></span>

### <span data-ttu-id="410c4-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="410c4-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="410c4-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="410c4-138">NOTES</span></span>

## <span data-ttu-id="410c4-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="410c4-139">RELATED LINKS</span></span>
