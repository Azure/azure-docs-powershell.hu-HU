---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161323"
---
# <span data-ttu-id="a3e57-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="a3e57-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="a3e57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e57-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e57-103">A távoli megjelenítési fiók kulcsának lekérte</span><span class="sxs-lookup"><span data-stu-id="a3e57-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="a3e57-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3e57-104">SYNTAX</span></span>

### <span data-ttu-id="a3e57-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3e57-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3e57-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3e57-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3e57-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3e57-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e57-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3e57-108">DESCRIPTION</span></span>
<span data-ttu-id="a3e57-109">Szerezze be a távoli leképezési fiók fejlesztői kulcsait.</span><span class="sxs-lookup"><span data-stu-id="a3e57-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="a3e57-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3e57-110">EXAMPLES</span></span>

### <span data-ttu-id="a3e57-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a3e57-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="a3e57-112">A távoli leképezési fiók "példa" fejlesztői kulcsait az aktuális Előfizetés és erőforráscsoport "rg1" csoportjából szerezze be.</span><span class="sxs-lookup"><span data-stu-id="a3e57-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="a3e57-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a3e57-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="a3e57-114">A távoli leképezési fiók "példa" fejlesztői kulcsait az aktuális Előfizetés és Erőforráscsoport "rg1" és pipázás használatával.</span><span class="sxs-lookup"><span data-stu-id="a3e57-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="a3e57-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3e57-115">PARAMETERS</span></span>

### <span data-ttu-id="a3e57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e57-116">-DefaultProfile</span></span>
<span data-ttu-id="a3e57-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3e57-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e57-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3e57-118">-InputObject</span></span>
<span data-ttu-id="a3e57-119">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="a3e57-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3e57-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a3e57-120">-Name</span></span>
<span data-ttu-id="a3e57-121">Távoli leképezési fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a3e57-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e57-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e57-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3e57-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a3e57-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e57-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3e57-124">-ResourceId</span></span>
<span data-ttu-id="a3e57-125">A távoli leképezési fiók erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3e57-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3e57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e57-126">CommonParameters</span></span>
<span data-ttu-id="a3e57-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3e57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a3e57-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3e57-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e57-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3e57-129">INPUTS</span></span>

### <span data-ttu-id="a3e57-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a3e57-130">System.String</span></span>

### <span data-ttu-id="a3e57-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="a3e57-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="a3e57-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3e57-132">OUTPUTS</span></span>

### <span data-ttu-id="a3e57-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a3e57-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="a3e57-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3e57-134">NOTES</span></span>

## <span data-ttu-id="a3e57-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3e57-135">RELATED LINKS</span></span>
