---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025656"
---
# <span data-ttu-id="e2990-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="e2990-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="e2990-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2990-102">SYNOPSIS</span></span>
<span data-ttu-id="e2990-103">A távoli megjelenítési fiók gombjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e2990-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="e2990-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2990-104">SYNTAX</span></span>

### <span data-ttu-id="e2990-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2990-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2990-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2990-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2990-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2990-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2990-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2990-108">DESCRIPTION</span></span>
<span data-ttu-id="e2990-109">A távoli megjelenítési fiók fejlesztői kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e2990-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="e2990-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e2990-110">EXAMPLES</span></span>

### <span data-ttu-id="e2990-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2990-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e2990-112">Az aktuális előfizetés és az erőforráscsoport "rg1" fejlesztői kulcsainak beszerzése "példa" a távoli megjelenítési fiókról.</span><span class="sxs-lookup"><span data-stu-id="e2990-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="e2990-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e2990-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e2990-114">A "rg1" "a jelenlegi előfizetés és az erőforráscsoport" "a csővezetékekkel" a távoli megjelenítési fiók fejlesztői kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e2990-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="e2990-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2990-115">PARAMETERS</span></span>

### <span data-ttu-id="e2990-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2990-116">-DefaultProfile</span></span>
<span data-ttu-id="e2990-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2990-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2990-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2990-118">-InputObject</span></span>
<span data-ttu-id="e2990-119">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="e2990-119">The custom domain object.</span></span>

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

### <span data-ttu-id="e2990-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2990-120">-Name</span></span>
<span data-ttu-id="e2990-121">Távoli megjelenítési fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e2990-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="e2990-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2990-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2990-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e2990-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="e2990-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2990-124">-ResourceId</span></span>
<span data-ttu-id="e2990-125">A távoli megjelenítési fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e2990-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="e2990-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2990-126">CommonParameters</span></span>
<span data-ttu-id="e2990-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2990-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e2990-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2990-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2990-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2990-129">INPUTS</span></span>

### <span data-ttu-id="e2990-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e2990-130">System.String</span></span>

### <span data-ttu-id="e2990-131">Microsoft. Azure. Command. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="e2990-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="e2990-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2990-132">OUTPUTS</span></span>

### <span data-ttu-id="e2990-133">Microsoft. Azure. Command. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e2990-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="e2990-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2990-134">NOTES</span></span>

## <span data-ttu-id="e2990-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2990-135">RELATED LINKS</span></span>
