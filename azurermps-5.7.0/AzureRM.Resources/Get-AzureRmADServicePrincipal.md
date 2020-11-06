---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8344d9e794189d67a69c1be9a88e135b721a0d4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494378"
---
# <span data-ttu-id="dc9ef-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dc9ef-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="dc9ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9ef-103">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc9ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc9ef-104">SYNTAX</span></span>

### <span data-ttu-id="dc9ef-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc9ef-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc9ef-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc9ef-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc9ef-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc9ef-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc9ef-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc9ef-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc9ef-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc9ef-109">DESCRIPTION</span></span>
<span data-ttu-id="dc9ef-110">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="dc9ef-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dc9ef-111">EXAMPLES</span></span>

### <span data-ttu-id="dc9ef-112">Szolgáltatás-résztvevők szűrése az SPN-lel</span><span class="sxs-lookup"><span data-stu-id="dc9ef-112">Filters service principals using SPN</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="dc9ef-113">A 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN-vel kapja meg a szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="dc9ef-114">A szolgáltatás-résztvevők szűrése keresési karakterlánccal</span><span class="sxs-lookup"><span data-stu-id="dc9ef-114">Filters service principals using Search String</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="dc9ef-115">Szűri az összes olyan ad-szolgáltatót, amelynél a megjelenítendő név "web" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="dc9ef-116">AD-szolgáltatói résztvevők listázása</span><span class="sxs-lookup"><span data-stu-id="dc9ef-116">List AD service principals</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="dc9ef-117">Beolvassa az összes AD Service-résztvevőt.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="dc9ef-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc9ef-118">PARAMETERS</span></span>

### <span data-ttu-id="dc9ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9ef-119">-DefaultProfile</span></span>
<span data-ttu-id="dc9ef-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dc9ef-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ef-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dc9ef-121">-ObjectId</span></span>
<span data-ttu-id="dc9ef-122">A szolgáltatás megbízójának objektumazonosító-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-122">Object id of the service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ef-123">-KeresendoString</span><span class="sxs-lookup"><span data-stu-id="dc9ef-123">-SearchString</span></span>
<span data-ttu-id="dc9ef-124">Beolvassa az összes olyan szolgáltatót, akinek az értéke a megjelenítendő névvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-124">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ef-125">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dc9ef-125">-ServicePrincipalName</span></span>
<span data-ttu-id="dc9ef-126">A szolgáltatás SPN-je.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-126">SPN of the service.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9ef-127">CommonParameters</span></span>
<span data-ttu-id="dc9ef-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc9ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9ef-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc9ef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9ef-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc9ef-130">INPUTS</span></span>

### <span data-ttu-id="dc9ef-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="dc9ef-131">None</span></span>
<span data-ttu-id="dc9ef-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="dc9ef-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc9ef-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc9ef-133">OUTPUTS</span></span>

### <span data-ttu-id="dc9ef-134">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="dc9ef-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="dc9ef-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc9ef-135">NOTES</span></span>

## <span data-ttu-id="dc9ef-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc9ef-136">RELATED LINKS</span></span>

[<span data-ttu-id="dc9ef-137">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dc9ef-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="dc9ef-138">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dc9ef-138">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="dc9ef-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dc9ef-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="dc9ef-140">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="dc9ef-140">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="dc9ef-141">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="dc9ef-141">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

