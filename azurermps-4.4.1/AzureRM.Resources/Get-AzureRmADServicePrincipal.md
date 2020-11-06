---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503963"
---
# <span data-ttu-id="93c65-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="93c65-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="93c65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93c65-102">SYNOPSIS</span></span>
<span data-ttu-id="93c65-103">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="93c65-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93c65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93c65-104">SYNTAX</span></span>

### <span data-ttu-id="93c65-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93c65-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93c65-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c65-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93c65-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c65-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93c65-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c65-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93c65-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="93c65-109">DESCRIPTION</span></span>
<span data-ttu-id="93c65-110">Szűri az Active Directory-szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="93c65-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="93c65-111">Példák</span><span class="sxs-lookup"><span data-stu-id="93c65-111">EXAMPLES</span></span>

### <span data-ttu-id="93c65-112">--------------------------Szűrők egyszerű szolgáltatásnév használatával--------------------------</span><span class="sxs-lookup"><span data-stu-id="93c65-112">--------------------------  Filters service principals using SPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="93c65-113">A 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN-vel kapja meg a szolgáltatási résztvevőket.</span><span class="sxs-lookup"><span data-stu-id="93c65-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="93c65-114">A--------------------------a keresési karakterlánccal szűri a szolgáltatás-résztvevőket--------------------------</span><span class="sxs-lookup"><span data-stu-id="93c65-114">--------------------------  Filters service principals using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="93c65-115">Szűri az összes olyan ad-szolgáltatót, amelynél a megjelenítendő név "web" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="93c65-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="93c65-116">--------------------------Lista AD-résztvevőknek--------------------------</span><span class="sxs-lookup"><span data-stu-id="93c65-116">--------------------------  List AD service principals  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="93c65-117">Beolvassa az összes AD Service-résztvevőt.</span><span class="sxs-lookup"><span data-stu-id="93c65-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="93c65-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93c65-118">PARAMETERS</span></span>

### <span data-ttu-id="93c65-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="93c65-119">-ObjectId</span></span>
<span data-ttu-id="93c65-120">A szolgáltatás megbízójának objektumazonosító-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93c65-120">Object id of the service principal.</span></span>

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

### <span data-ttu-id="93c65-121">-KeresendoString</span><span class="sxs-lookup"><span data-stu-id="93c65-121">-SearchString</span></span>
<span data-ttu-id="93c65-122">Beolvassa az összes olyan szolgáltatót, akinek az értéke a megjelenítendő névvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="93c65-122">Fetches all service principals that have the display name starting with this value.</span></span>

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

### <span data-ttu-id="93c65-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="93c65-123">-ServicePrincipalName</span></span>
<span data-ttu-id="93c65-124">A szolgáltatás SPN-je.</span><span class="sxs-lookup"><span data-stu-id="93c65-124">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c65-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c65-125">-DefaultProfile</span></span>
<span data-ttu-id="93c65-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93c65-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93c65-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c65-127">CommonParameters</span></span>
<span data-ttu-id="93c65-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93c65-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c65-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c65-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c65-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93c65-130">INPUTS</span></span>

## <span data-ttu-id="93c65-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93c65-131">OUTPUTS</span></span>

### <span data-ttu-id="93c65-132">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="93c65-132">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="93c65-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93c65-133">NOTES</span></span>

## <span data-ttu-id="93c65-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93c65-134">RELATED LINKS</span></span>

[<span data-ttu-id="93c65-135">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="93c65-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="93c65-136">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="93c65-136">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="93c65-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="93c65-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="93c65-138">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="93c65-138">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="93c65-139">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="93c65-139">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

