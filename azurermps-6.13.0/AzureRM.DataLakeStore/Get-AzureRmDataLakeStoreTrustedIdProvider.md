---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 07bcfff4ab8d1e071ed34c9a52e8aa4e98c32946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494064"
---
# <span data-ttu-id="d27da-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d27da-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d27da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d27da-102">SYNOPSIS</span></span>
<span data-ttu-id="d27da-103">A megadott adattárolóban kapja meg a megadott megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="d27da-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="d27da-104">Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.</span><span class="sxs-lookup"><span data-stu-id="d27da-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d27da-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d27da-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d27da-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="d27da-106">DESCRIPTION</span></span>
<span data-ttu-id="d27da-107">A **Get-AzureRmDataLakeStoreTrustedIdProvider** parancsmag a megadott adattó-tárolóban kapja meg a megadott megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="d27da-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="d27da-108">Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.</span><span class="sxs-lookup"><span data-stu-id="d27da-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="d27da-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d27da-109">EXAMPLES</span></span>

### <span data-ttu-id="d27da-110">1. példa: konkrét megbízható identitás-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="d27da-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="d27da-111">A "MyProvider" nevű szolgáltatót számítja ki a "ContosoADL" fiókból.</span><span class="sxs-lookup"><span data-stu-id="d27da-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="d27da-112">2. példa: a fiók összes szolgáltatójának listázása</span><span class="sxs-lookup"><span data-stu-id="d27da-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="d27da-113">A "ContosoADL" fiók alatti összes szolgáltató felsorolása</span><span class="sxs-lookup"><span data-stu-id="d27da-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="d27da-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d27da-114">PARAMETERS</span></span>

### <span data-ttu-id="d27da-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="d27da-115">-Account</span></span>
<span data-ttu-id="d27da-116">Az adattó-tároló fiók a megbízható identitás-szolgáltató beolvasásához</span><span class="sxs-lookup"><span data-stu-id="d27da-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="d27da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27da-117">-DefaultProfile</span></span>
<span data-ttu-id="d27da-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d27da-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d27da-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d27da-119">-Name</span></span>
<span data-ttu-id="d27da-120">A lekérdezni kívánt megbízható identitás-szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="d27da-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="d27da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d27da-121">-ResourceGroupName</span></span>
<span data-ttu-id="d27da-122">Annak az erőforráscsoportnek a neve, amely alatt a megadott fiók megadott megbízható identitás-szolgáltatóját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="d27da-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="d27da-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27da-123">CommonParameters</span></span>
<span data-ttu-id="d27da-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d27da-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27da-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d27da-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27da-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d27da-126">INPUTS</span></span>

### <span data-ttu-id="d27da-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d27da-127">System.String</span></span>

## <span data-ttu-id="d27da-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d27da-128">OUTPUTS</span></span>

### <span data-ttu-id="d27da-129">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d27da-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d27da-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d27da-130">NOTES</span></span>

## <span data-ttu-id="d27da-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d27da-131">RELATED LINKS</span></span>
