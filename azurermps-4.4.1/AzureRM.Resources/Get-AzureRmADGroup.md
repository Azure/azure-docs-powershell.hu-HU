---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494702"
---
# <span data-ttu-id="c8418-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="c8418-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="c8418-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8418-102">SYNOPSIS</span></span>
<span data-ttu-id="c8418-103">Szűri az Active Directory-csoportokat.</span><span class="sxs-lookup"><span data-stu-id="c8418-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8418-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8418-104">SYNTAX</span></span>

### <span data-ttu-id="c8418-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8418-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8418-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8418-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8418-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8418-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8418-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8418-108">DESCRIPTION</span></span>
<span data-ttu-id="c8418-109">Szűri az Active Directory-csoportokat.</span><span class="sxs-lookup"><span data-stu-id="c8418-109">Filters active directory groups.</span></span>

## <span data-ttu-id="c8418-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c8418-110">EXAMPLES</span></span>

### <span data-ttu-id="c8418-111">A csoportok szűrése--------------------------objektum-azonosítóval--------------------------</span><span class="sxs-lookup"><span data-stu-id="c8418-111">--------------------------  Filters groups using object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c8418-112">Csoport beolvasása 85F89C90-780E-4AA6-9F4F-6F268D322EEE-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="c8418-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="c8418-113">A--------------------------a keresési karakterlánccal szűri a csoportokat--------------------------</span><span class="sxs-lookup"><span data-stu-id="c8418-113">--------------------------  Filters groups using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="c8418-114">Az összes olyan hirdetéscsoportot szűri, amely a megjelenített névvel rendelkezik Joe-val.</span><span class="sxs-lookup"><span data-stu-id="c8418-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="c8418-115">--------------------------Lista AD-csoportok--------------------------</span><span class="sxs-lookup"><span data-stu-id="c8418-115">--------------------------  List AD groups  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="c8418-116">Minden HIRDETÉSCSOPORT beolvasása</span><span class="sxs-lookup"><span data-stu-id="c8418-116">Gets all AD groups</span></span>

## <span data-ttu-id="c8418-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8418-117">PARAMETERS</span></span>

### <span data-ttu-id="c8418-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c8418-118">-ObjectId</span></span>
<span data-ttu-id="c8418-119">A csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c8418-119">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8418-120">-KeresendoString</span><span class="sxs-lookup"><span data-stu-id="c8418-120">-SearchString</span></span>
<span data-ttu-id="c8418-121">A csoport megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="c8418-121">The group display name</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8418-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8418-122">-DefaultProfile</span></span>
<span data-ttu-id="c8418-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8418-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8418-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8418-124">CommonParameters</span></span>
<span data-ttu-id="c8418-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8418-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8418-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8418-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8418-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8418-127">INPUTS</span></span>

## <span data-ttu-id="c8418-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8418-128">OUTPUTS</span></span>

### <span data-ttu-id="c8418-129">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="c8418-129">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="c8418-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8418-130">NOTES</span></span>

## <span data-ttu-id="c8418-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8418-131">RELATED LINKS</span></span>

[<span data-ttu-id="c8418-132">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c8418-132">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="c8418-133">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8418-133">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c8418-134">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="c8418-134">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

