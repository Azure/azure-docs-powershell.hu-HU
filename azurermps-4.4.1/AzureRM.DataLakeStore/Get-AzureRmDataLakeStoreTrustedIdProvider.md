---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: e95fd5e487fc29a40e48484b0a905def8356e260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501899"
---
# <span data-ttu-id="4bd5a-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4bd5a-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4bd5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bd5a-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd5a-103">A megadott adattárolóban kapja meg a megadott megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="4bd5a-104">Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd5a-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bd5a-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd5a-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bd5a-106">DESCRIPTION</span></span>
<span data-ttu-id="4bd5a-107">A **Get-AzureRmDataLakeStoreTrustedIdProvider** parancsmag a megadott adattó-tárolóban kapja meg a megadott megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="4bd5a-108">Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="4bd5a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4bd5a-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd5a-110">1. példa: konkrét megbízható identitás-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="4bd5a-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="4bd5a-111">A "MyProvider" nevű szolgáltatót számítja ki a "ContosoADL" fiókból.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="4bd5a-112">2. példa: a fiók összes szolgáltatójának listázása</span><span class="sxs-lookup"><span data-stu-id="4bd5a-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="4bd5a-113">A "ContosoADL" fiók alatti összes szolgáltató felsorolása</span><span class="sxs-lookup"><span data-stu-id="4bd5a-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="4bd5a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bd5a-114">PARAMETERS</span></span>

### <span data-ttu-id="4bd5a-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="4bd5a-115">-Account</span></span>
<span data-ttu-id="4bd5a-116">Az adattó-tároló fiók a megbízható identitás-szolgáltató beolvasásához</span><span class="sxs-lookup"><span data-stu-id="4bd5a-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd5a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4bd5a-117">-Name</span></span>
<span data-ttu-id="4bd5a-118">A lekérdezni kívánt megbízható identitás-szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="4bd5a-118">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd5a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd5a-119">-ResourceGroupName</span></span>
<span data-ttu-id="4bd5a-120">Annak az erőforráscsoportnek a neve, amely alatt a megadott fiók megadott megbízható identitás-szolgáltatóját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-120">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd5a-121">-DefaultProfile</span></span>
<span data-ttu-id="4bd5a-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bd5a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd5a-123">CommonParameters</span></span>
<span data-ttu-id="4bd5a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bd5a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd5a-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd5a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd5a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bd5a-126">INPUTS</span></span>

## <span data-ttu-id="4bd5a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bd5a-127">OUTPUTS</span></span>

### <span data-ttu-id="4bd5a-128">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4bd5a-128">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="4bd5a-129">A megadott megbízható identitás-szolgáltató adatai.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-129">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="4bd5a-130">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="4bd5a-130">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="4bd5a-131">A megadott fiók megbízható identitás-szolgáltatóinak listája.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-131">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="4bd5a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bd5a-132">NOTES</span></span>

## <span data-ttu-id="4bd5a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bd5a-133">RELATED LINKS</span></span>

