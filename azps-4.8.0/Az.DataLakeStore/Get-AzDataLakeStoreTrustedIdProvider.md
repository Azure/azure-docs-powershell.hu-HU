---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017848"
---
# <span data-ttu-id="61969-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="61969-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="61969-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61969-102">SYNOPSIS</span></span>
<span data-ttu-id="61969-103">A megadott adattárolóban kapja meg a megadott megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="61969-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="61969-104">Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.</span><span class="sxs-lookup"><span data-stu-id="61969-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="61969-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61969-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61969-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="61969-106">DESCRIPTION</span></span>
<span data-ttu-id="61969-107">A **Get-AzDataLakeStoreTrustedIdProvider** parancsmag a megadott adattó-tárolóban kapja meg a megadott megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="61969-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="61969-108">Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.</span><span class="sxs-lookup"><span data-stu-id="61969-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="61969-109">Példák</span><span class="sxs-lookup"><span data-stu-id="61969-109">EXAMPLES</span></span>

### <span data-ttu-id="61969-110">1. példa: konkrét megbízható identitás-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="61969-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="61969-111">A "MyProvider" nevű szolgáltatót számítja ki a "ContosoADL" fiókból.</span><span class="sxs-lookup"><span data-stu-id="61969-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="61969-112">2. példa: a fiók összes szolgáltatójának listázása</span><span class="sxs-lookup"><span data-stu-id="61969-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="61969-113">A "ContosoADL" fiók alatti összes szolgáltató felsorolása</span><span class="sxs-lookup"><span data-stu-id="61969-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="61969-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61969-114">PARAMETERS</span></span>

### <span data-ttu-id="61969-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="61969-115">-Account</span></span>
<span data-ttu-id="61969-116">Az adattó-tároló fiók a megbízható identitás-szolgáltató beolvasásához</span><span class="sxs-lookup"><span data-stu-id="61969-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="61969-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61969-117">-DefaultProfile</span></span>
<span data-ttu-id="61969-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="61969-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61969-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61969-119">-Name</span></span>
<span data-ttu-id="61969-120">A lekérdezni kívánt megbízható identitás-szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="61969-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="61969-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61969-121">-ResourceGroupName</span></span>
<span data-ttu-id="61969-122">Annak az erőforráscsoportnek a neve, amely alatt a megadott fiók megadott megbízható identitás-szolgáltatóját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="61969-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="61969-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61969-123">CommonParameters</span></span>
<span data-ttu-id="61969-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61969-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61969-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61969-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61969-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61969-126">INPUTS</span></span>

### <span data-ttu-id="61969-127">System. String</span><span class="sxs-lookup"><span data-stu-id="61969-127">System.String</span></span>

## <span data-ttu-id="61969-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61969-128">OUTPUTS</span></span>

### <span data-ttu-id="61969-129">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="61969-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="61969-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61969-130">NOTES</span></span>

## <span data-ttu-id="61969-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61969-131">RELATED LINKS</span></span>
