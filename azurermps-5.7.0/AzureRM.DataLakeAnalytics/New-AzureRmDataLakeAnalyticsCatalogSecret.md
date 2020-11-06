---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 838ebb56f52aa34bc1fe6016a8bf4f4966f4428d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494525"
---
# <span data-ttu-id="226ec-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="226ec-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="226ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="226ec-102">SYNOPSIS</span></span>
<span data-ttu-id="226ec-103">Létrehoz egy adattó-adatforrást, amelynek a katalógusa titkos.</span><span class="sxs-lookup"><span data-stu-id="226ec-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="226ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="226ec-104">SYNTAX</span></span>

### <span data-ttu-id="226ec-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="226ec-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="226ec-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="226ec-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="226ec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="226ec-107">DESCRIPTION</span></span>
<span data-ttu-id="226ec-108">A **New-AzureRmDataLakeAnalyticsCatalogSecret** parancsmag titkot hoz létre az Azure Data Lake Analytics katalógusban való használathoz.</span><span class="sxs-lookup"><span data-stu-id="226ec-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="226ec-109">Példák</span><span class="sxs-lookup"><span data-stu-id="226ec-109">EXAMPLES</span></span>

### <span data-ttu-id="226ec-110">Példa 1: a katalógus titkának beszerzése</span><span class="sxs-lookup"><span data-stu-id="226ec-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="226ec-111">Ez a parancs a megadott fiókhoz, adatbázishoz, hitelesítő adatokhoz vagy állomáshoz tartozó titkot kapja.</span><span class="sxs-lookup"><span data-stu-id="226ec-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="226ec-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="226ec-112">PARAMETERS</span></span>

### <span data-ttu-id="226ec-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="226ec-113">-Account</span></span>
<span data-ttu-id="226ec-114">Az adattó-Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="226ec-114">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="226ec-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="226ec-115">-DatabaseHost</span></span>
<span data-ttu-id="226ec-116">Annak az adatbázisnak az állomásnevét adja meg, amelynek a titka az "mydatabase.contoso.com" formátumban van társítva.</span><span class="sxs-lookup"><span data-stu-id="226ec-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226ec-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="226ec-117">-DatabaseName</span></span>
<span data-ttu-id="226ec-118">A titkot birtokló adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="226ec-118">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226ec-119">-DefaultProfile</span></span>
<span data-ttu-id="226ec-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="226ec-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="226ec-121">-Port</span><span class="sxs-lookup"><span data-stu-id="226ec-121">-Port</span></span>
<span data-ttu-id="226ec-122">A titok portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="226ec-122">Specifies the port number of the secret.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226ec-123">-Secret</span><span class="sxs-lookup"><span data-stu-id="226ec-123">-Secret</span></span>
<span data-ttu-id="226ec-124">A titok nevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="226ec-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226ec-125">-URI</span><span class="sxs-lookup"><span data-stu-id="226ec-125">-Uri</span></span>
<span data-ttu-id="226ec-126">A titok egységes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="226ec-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: Uri
Parameter Sets: CreateByHostNameAndPort
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226ec-127">CommonParameters</span></span>
<span data-ttu-id="226ec-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="226ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226ec-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="226ec-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226ec-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="226ec-130">INPUTS</span></span>

### <span data-ttu-id="226ec-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="226ec-131">None</span></span>
<span data-ttu-id="226ec-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="226ec-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="226ec-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="226ec-133">OUTPUTS</span></span>

### <span data-ttu-id="226ec-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="226ec-134">None</span></span>

## <span data-ttu-id="226ec-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="226ec-135">NOTES</span></span>

## <span data-ttu-id="226ec-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="226ec-136">RELATED LINKS</span></span>

[<span data-ttu-id="226ec-137">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="226ec-137">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="226ec-138">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="226ec-138">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


