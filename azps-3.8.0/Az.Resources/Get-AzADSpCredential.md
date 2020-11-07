---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846810"
---
# <span data-ttu-id="2461c-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2461c-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="2461c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2461c-102">SYNOPSIS</span></span>
<span data-ttu-id="2461c-103">Lekérdezi a szolgáltatóhoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="2461c-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="2461c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2461c-104">SYNTAX</span></span>

### <span data-ttu-id="2461c-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2461c-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2461c-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2461c-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2461c-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2461c-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2461c-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2461c-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2461c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2461c-109">DESCRIPTION</span></span>
<span data-ttu-id="2461c-110">A Get-AzADSpCredential parancsmag használatával lekérdezheti a szolgáltatóhoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="2461c-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="2461c-111">Ez a parancs a szolgáltatóhoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja visszakeresni.</span><span class="sxs-lookup"><span data-stu-id="2461c-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="2461c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2461c-112">EXAMPLES</span></span>

### <span data-ttu-id="2461c-113">Példa 1 – a hitelesítő adatok listázása SPN szerint</span><span class="sxs-lookup"><span data-stu-id="2461c-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="2461c-114">Az SPN-vel rendelkező szolgáltatóhoz társított hitelesítő adatok listáját számítja ki http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="2461c-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="2461c-115">Példa 2 – objektumazonosító szerint a hitelesítő adatok listája</span><span class="sxs-lookup"><span data-stu-id="2461c-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="2461c-116">A "58e28616-99cc-4da4-b705-7672130e1047" azonosítójú azonosítójú szolgáltatóhoz társított hitelesítő adatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2461c-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="2461c-117">Példa: 3 – a hitelesítő adatok listázása csővezeték szerint</span><span class="sxs-lookup"><span data-stu-id="2461c-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="2461c-118">Megkapja a "58e28616-99cc-4da4-b705-7672130e1047" azonosítójú szolgáltatásnevet, és az Get-AzADSpCredential parancsmaghoz beilleszti az adott szolgáltatáshoz tartozó hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="2461c-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="2461c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2461c-119">PARAMETERS</span></span>

### <span data-ttu-id="2461c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2461c-120">-DefaultProfile</span></span>
<span data-ttu-id="2461c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2461c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2461c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2461c-122">-DisplayName</span></span>
<span data-ttu-id="2461c-123">A szolgáltatás megbízójának megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="2461c-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2461c-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2461c-124">-ObjectId</span></span>
<span data-ttu-id="2461c-125">A szolgáltatás megbízójának objektum azonosítója a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="2461c-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2461c-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2461c-126">-ServicePrincipalName</span></span>
<span data-ttu-id="2461c-127">A szolgáltatás megbízójának neve (SPN) a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="2461c-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2461c-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="2461c-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="2461c-129">A Service Principal objektum a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="2461c-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2461c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2461c-130">CommonParameters</span></span>
<span data-ttu-id="2461c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2461c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2461c-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2461c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2461c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2461c-133">INPUTS</span></span>

### <span data-ttu-id="2461c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2461c-134">System.String</span></span>

### <span data-ttu-id="2461c-135">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2461c-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2461c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2461c-136">OUTPUTS</span></span>

### <span data-ttu-id="2461c-137">Microsoft. Azure. Command. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="2461c-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="2461c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2461c-138">NOTES</span></span>

## <span data-ttu-id="2461c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2461c-139">RELATED LINKS</span></span>

[<span data-ttu-id="2461c-140">Új – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2461c-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="2461c-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2461c-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="2461c-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2461c-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)
