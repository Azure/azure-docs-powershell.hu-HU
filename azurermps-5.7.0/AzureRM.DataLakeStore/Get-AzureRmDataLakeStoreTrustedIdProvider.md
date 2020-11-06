---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c387ebb089ab7f9dfddaee818f26596f34ed91e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503776"
---
# <span data-ttu-id="7dbda-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="7dbda-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="7dbda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7dbda-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbda-103">A megadott adattárolóban kapja meg a megadott megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="7dbda-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="7dbda-104">Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.</span><span class="sxs-lookup"><span data-stu-id="7dbda-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dbda-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7dbda-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dbda-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="7dbda-106">DESCRIPTION</span></span>
<span data-ttu-id="7dbda-107">A **Get-AzureRmDataLakeStoreTrustedIdProvider** parancsmag a megadott adattó-tárolóban kapja meg a megadott megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="7dbda-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="7dbda-108">Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.</span><span class="sxs-lookup"><span data-stu-id="7dbda-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="7dbda-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7dbda-109">EXAMPLES</span></span>

### <span data-ttu-id="7dbda-110">1. példa: konkrét megbízható identitás-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="7dbda-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="7dbda-111">A "MyProvider" nevű szolgáltatót számítja ki a "ContosoADL" fiókból.</span><span class="sxs-lookup"><span data-stu-id="7dbda-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="7dbda-112">2. példa: a fiók összes szolgáltatójának listázása</span><span class="sxs-lookup"><span data-stu-id="7dbda-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="7dbda-113">A "ContosoADL" fiók alatti összes szolgáltató felsorolása</span><span class="sxs-lookup"><span data-stu-id="7dbda-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="7dbda-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7dbda-114">PARAMETERS</span></span>

### <span data-ttu-id="7dbda-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="7dbda-115">-Account</span></span>
<span data-ttu-id="7dbda-116">Az adattó-tároló fiók a megbízható identitás-szolgáltató beolvasásához</span><span class="sxs-lookup"><span data-stu-id="7dbda-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbda-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbda-117">-DefaultProfile</span></span>
<span data-ttu-id="7dbda-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7dbda-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dbda-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7dbda-119">-Name</span></span>
<span data-ttu-id="7dbda-120">A lekérdezni kívánt megbízható identitás-szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="7dbda-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbda-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dbda-121">-ResourceGroupName</span></span>
<span data-ttu-id="7dbda-122">Annak az erőforráscsoportnek a neve, amely alatt a megadott fiók megadott megbízható identitás-szolgáltatóját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="7dbda-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbda-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbda-123">CommonParameters</span></span>
<span data-ttu-id="7dbda-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7dbda-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbda-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dbda-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbda-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dbda-126">INPUTS</span></span>

### <span data-ttu-id="7dbda-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="7dbda-127">None</span></span>
<span data-ttu-id="7dbda-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7dbda-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7dbda-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dbda-129">OUTPUTS</span></span>

### <span data-ttu-id="7dbda-130">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="7dbda-130">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="7dbda-131">A megadott megbízható identitás-szolgáltató adatai.</span><span class="sxs-lookup"><span data-stu-id="7dbda-131">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="7dbda-132">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="7dbda-132">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="7dbda-133">A megadott fiók megbízható identitás-szolgáltatóinak listája.</span><span class="sxs-lookup"><span data-stu-id="7dbda-133">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="7dbda-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7dbda-134">NOTES</span></span>

## <span data-ttu-id="7dbda-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7dbda-135">RELATED LINKS</span></span>

