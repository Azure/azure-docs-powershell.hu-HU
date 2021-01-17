---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342269"
---
# <span data-ttu-id="2c9c3-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2c9c3-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="2c9c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c9c3-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9c3-103">Beveszi a fiókot.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-103">Gets the account.</span></span>

## <span data-ttu-id="2c9c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c9c3-104">SYNTAX</span></span>

### <span data-ttu-id="2c9c3-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c9c3-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c9c3-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c9c3-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c9c3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c9c3-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c9c3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c9c3-108">DESCRIPTION</span></span>
<span data-ttu-id="2c9c3-109">A Get-AzMapsAccount egy kiépített Azure Maps-fiókot kap, akár erőforráscsoport, akár név, akár erőforrás-azonosító alapján. Ezenkívül az erőforráscsoport összes fiókja, illetve az aktuális előfizetéshez az összes Azure Maps-fiók listáját is visszaadhatja.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="2c9c3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c9c3-110">EXAMPLES</span></span>

### <span data-ttu-id="2c9c3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2c9c3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="2c9c3-112">A MyResourceGroup erőforráscsoport MyAccount nevű fiókjának lekérte, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="2c9c3-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2c9c3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="2c9c3-114">Beveszi a MyResourceGroup erőforráscsoport összes Azure Maps-fiókot.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="2c9c3-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="2c9c3-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="2c9c3-116">Az aktuális előfizetésben lévő összes Azure Maps-fiókot beveszi.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="2c9c3-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="2c9c3-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="2c9c3-118">Beveszi az Erőforrás-azonosító által megadott Térképek-fiókot.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="2c9c3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c9c3-119">PARAMETERS</span></span>

### <span data-ttu-id="2c9c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9c3-120">-DefaultProfile</span></span>
<span data-ttu-id="2c9c3-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c9c3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2c9c3-122">-Name</span></span>
<span data-ttu-id="2c9c3-123">Térképek-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c9c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="2c9c3-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9c3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c9c3-126">-ResourceId</span></span>
<span data-ttu-id="2c9c3-127">Leképezi a Fiók erőforrásazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="2c9c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9c3-128">CommonParameters</span></span>
<span data-ttu-id="2c9c3-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9c3-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9c3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9c3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c9c3-131">INPUTS</span></span>

### <span data-ttu-id="2c9c3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2c9c3-132">System.String</span></span>

## <span data-ttu-id="2c9c3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c9c3-133">OUTPUTS</span></span>

### <span data-ttu-id="2c9c3-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2c9c3-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="2c9c3-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c9c3-135">NOTES</span></span>

## <span data-ttu-id="2c9c3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c9c3-136">RELATED LINKS</span></span>
