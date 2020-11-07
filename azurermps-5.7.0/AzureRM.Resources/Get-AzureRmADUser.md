---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678946"
---
# <span data-ttu-id="de400-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="de400-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="de400-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de400-102">SYNOPSIS</span></span>
<span data-ttu-id="de400-103">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="de400-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de400-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de400-104">SYNTAX</span></span>

### <span data-ttu-id="de400-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de400-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de400-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="de400-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de400-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de400-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de400-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="de400-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de400-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="de400-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de400-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="de400-110">DESCRIPTION</span></span>
<span data-ttu-id="de400-111">Szűri az Active Directory felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="de400-111">Filters active directory users.</span></span>

## <span data-ttu-id="de400-112">Példák</span><span class="sxs-lookup"><span data-stu-id="de400-112">EXAMPLES</span></span>

### <span data-ttu-id="de400-113">Felhasználók szűrése UPN használatával</span><span class="sxs-lookup"><span data-stu-id="de400-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="de400-114">Felhasználó kapja meg a foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="de400-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="de400-115">Felhasználók szűrése a keresési karakterlánccal</span><span class="sxs-lookup"><span data-stu-id="de400-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="de400-116">A megjelenített nevében Joe-t használó összes ad-felhasználó szűrése.</span><span class="sxs-lookup"><span data-stu-id="de400-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="de400-117">AD-felhasználók listázása</span><span class="sxs-lookup"><span data-stu-id="de400-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="de400-118">Minden AD-felhasználó beolvasása</span><span class="sxs-lookup"><span data-stu-id="de400-118">Gets all AD users</span></span>

## <span data-ttu-id="de400-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de400-119">PARAMETERS</span></span>

### <span data-ttu-id="de400-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de400-120">-DefaultProfile</span></span>
<span data-ttu-id="de400-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="de400-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de400-122">-Mail</span><span class="sxs-lookup"><span data-stu-id="de400-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de400-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="de400-123">-ObjectId</span></span>
<span data-ttu-id="de400-124">A felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="de400-124">Object id of the user.</span></span>

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

### <span data-ttu-id="de400-125">-KeresendoString</span><span class="sxs-lookup"><span data-stu-id="de400-125">-SearchString</span></span>
<span data-ttu-id="de400-126">A felhasználó megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="de400-126">The user display name</span></span>

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

### <span data-ttu-id="de400-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="de400-127">-UserPrincipalName</span></span>
<span data-ttu-id="de400-128">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="de400-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de400-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de400-129">CommonParameters</span></span>
<span data-ttu-id="de400-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de400-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de400-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de400-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de400-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de400-132">INPUTS</span></span>

### <span data-ttu-id="de400-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="de400-133">None</span></span>
<span data-ttu-id="de400-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="de400-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de400-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de400-135">OUTPUTS</span></span>

### <span data-ttu-id="de400-136">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="de400-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="de400-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de400-137">NOTES</span></span>

## <span data-ttu-id="de400-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de400-138">RELATED LINKS</span></span>

[<span data-ttu-id="de400-139">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="de400-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="de400-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="de400-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="de400-141">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="de400-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

