---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 8c03dd19fd2995347a3b4ae52de04fdcb3f02c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672844"
---
# <span data-ttu-id="f51ed-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f51ed-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="f51ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f51ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f51ed-103">Lekérdezi a szolgáltatóhoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="f51ed-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f51ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f51ed-104">SYNTAX</span></span>

### <span data-ttu-id="f51ed-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f51ed-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f51ed-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f51ed-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f51ed-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f51ed-107">DESCRIPTION</span></span>
<span data-ttu-id="f51ed-108">A Get-AzureRmADSpCredential parancsmag használatával lekérdezheti a szolgáltatóhoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="f51ed-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="f51ed-109">Ez a parancs a szolgáltatóhoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja visszakeresni.</span><span class="sxs-lookup"><span data-stu-id="f51ed-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="f51ed-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f51ed-110">EXAMPLES</span></span>

### <span data-ttu-id="f51ed-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f51ed-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="f51ed-112">Az SPN-t tartalmazó szolgáltatóhoz társított hitelesítő adatok listáját számítja ki http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="f51ed-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="f51ed-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f51ed-113">PARAMETERS</span></span>

### <span data-ttu-id="f51ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f51ed-114">-DefaultProfile</span></span>
<span data-ttu-id="f51ed-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f51ed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f51ed-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f51ed-116">-ObjectId</span></span>
<span data-ttu-id="f51ed-117">A szolgáltatás megbízójának objektum azonosítója a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="f51ed-117">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f51ed-118">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f51ed-118">-ServicePrincipalName</span></span>
<span data-ttu-id="f51ed-119">A szolgáltatás megbízójának neve (SPN) a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="f51ed-119">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f51ed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51ed-120">CommonParameters</span></span>
<span data-ttu-id="f51ed-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f51ed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51ed-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f51ed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51ed-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f51ed-123">INPUTS</span></span>

### <span data-ttu-id="f51ed-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="f51ed-124">None</span></span>
<span data-ttu-id="f51ed-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f51ed-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f51ed-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f51ed-126">OUTPUTS</span></span>

### <span data-ttu-id="f51ed-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="f51ed-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="f51ed-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f51ed-128">NOTES</span></span>

## <span data-ttu-id="f51ed-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f51ed-129">RELATED LINKS</span></span>

[<span data-ttu-id="f51ed-130">Új – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f51ed-130">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="f51ed-131">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f51ed-131">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="f51ed-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f51ed-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

