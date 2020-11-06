---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: dd864d11608c33f758e0995d9dacf4afc454130a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493376"
---
# <span data-ttu-id="bf105-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="bf105-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="bf105-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf105-102">SYNOPSIS</span></span>
<span data-ttu-id="bf105-103">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="bf105-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf105-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf105-104">SYNTAX</span></span>

### <span data-ttu-id="bf105-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf105-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf105-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf105-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf105-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf105-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf105-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf105-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf105-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf105-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf105-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf105-110">DESCRIPTION</span></span>
<span data-ttu-id="bf105-111">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="bf105-111">Filters active directory users.</span></span>

## <span data-ttu-id="bf105-112">Példák</span><span class="sxs-lookup"><span data-stu-id="bf105-112">EXAMPLES</span></span>

### <span data-ttu-id="bf105-113">--------------------------Szűrők használata UPN---------------------------</span><span class="sxs-lookup"><span data-stu-id="bf105-113">--------------------------  Filters users using UPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="bf105-114">Felhasználó kapja meg a foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="bf105-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="bf105-115">A felhasználók a keresési karakterlánccal--------------------------szűrők--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf105-115">--------------------------  Filters users using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="bf105-116">A megjelenített nevében Joe-t használó összes ad-felhasználó szűrése.</span><span class="sxs-lookup"><span data-stu-id="bf105-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="bf105-117">--------------------------Lista AD users--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf105-117">--------------------------  List AD users  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="bf105-118">Minden AD-felhasználó beolvasása</span><span class="sxs-lookup"><span data-stu-id="bf105-118">Gets all AD users</span></span>

## <span data-ttu-id="bf105-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf105-119">PARAMETERS</span></span>

### <span data-ttu-id="bf105-120">-Mail</span><span class="sxs-lookup"><span data-stu-id="bf105-120">-Mail</span></span>
```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf105-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bf105-121">-ObjectId</span></span>
<span data-ttu-id="bf105-122">A felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bf105-122">Object id of the user.</span></span>

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

### <span data-ttu-id="bf105-123">-KeresendoString</span><span class="sxs-lookup"><span data-stu-id="bf105-123">-SearchString</span></span>
<span data-ttu-id="bf105-124">A felhasználó megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="bf105-124">The user display name</span></span>

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

### <span data-ttu-id="bf105-125">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf105-125">-UserPrincipalName</span></span>
<span data-ttu-id="bf105-126">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="bf105-126">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf105-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf105-127">-DefaultProfile</span></span>
<span data-ttu-id="bf105-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf105-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf105-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf105-129">CommonParameters</span></span>
<span data-ttu-id="bf105-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf105-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf105-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf105-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf105-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf105-132">INPUTS</span></span>

## <span data-ttu-id="bf105-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf105-133">OUTPUTS</span></span>

### <span data-ttu-id="bf105-134">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="bf105-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="bf105-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf105-135">NOTES</span></span>

## <span data-ttu-id="bf105-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf105-136">RELATED LINKS</span></span>

[<span data-ttu-id="bf105-137">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="bf105-137">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="bf105-138">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="bf105-138">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="bf105-139">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="bf105-139">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

