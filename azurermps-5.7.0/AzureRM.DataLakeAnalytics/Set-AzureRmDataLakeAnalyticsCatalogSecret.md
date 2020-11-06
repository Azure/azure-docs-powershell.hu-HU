---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: cce57a2437a5e1fa0f440986534a11c1ab6c73ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495391"
---
# <span data-ttu-id="e5030-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e5030-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="e5030-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5030-102">SYNOPSIS</span></span>
<span data-ttu-id="e5030-103">Módosította az adattó-statisztika-katalógus titkát.</span><span class="sxs-lookup"><span data-stu-id="e5030-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5030-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5030-104">SYNTAX</span></span>

### <span data-ttu-id="e5030-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="e5030-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5030-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="e5030-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5030-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5030-107">DESCRIPTION</span></span>
<span data-ttu-id="e5030-108">A **set-AzureRmDataLakeAnalyticsCatalogSecret** parancsmag módosította az Azure Data Lake-Lake Analytics-katalógushoz társított titkot.</span><span class="sxs-lookup"><span data-stu-id="e5030-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="e5030-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e5030-109">EXAMPLES</span></span>

### <span data-ttu-id="e5030-110">Példa 1: egy fiókkal társított titok módosítása</span><span class="sxs-lookup"><span data-stu-id="e5030-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="e5030-111">Ez a parancs a Data Lake Analytics-katalógushoz társított titkot állítja be.</span><span class="sxs-lookup"><span data-stu-id="e5030-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="e5030-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5030-112">PARAMETERS</span></span>

### <span data-ttu-id="e5030-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="e5030-113">-Account</span></span>
<span data-ttu-id="e5030-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5030-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e5030-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="e5030-115">-DatabaseHost</span></span>
<span data-ttu-id="e5030-116">Annak az adatbázisnak az állomásnevét adja meg, amelynek a titka az "mydatabase.contoso.com" formátumban van társítva.</span><span class="sxs-lookup"><span data-stu-id="e5030-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5030-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e5030-117">-DatabaseName</span></span>
<span data-ttu-id="e5030-118">A titkot birtokló adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5030-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="e5030-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5030-119">-DefaultProfile</span></span>
<span data-ttu-id="e5030-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5030-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5030-121">-Port</span><span class="sxs-lookup"><span data-stu-id="e5030-121">-Port</span></span>
<span data-ttu-id="e5030-122">A titok portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5030-122">Specifies the port number of the secret.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByFullUri
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5030-123">-Secret</span><span class="sxs-lookup"><span data-stu-id="e5030-123">-Secret</span></span>
<span data-ttu-id="e5030-124">A titok nevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5030-124">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="e5030-125">-URI</span><span class="sxs-lookup"><span data-stu-id="e5030-125">-Uri</span></span>
<span data-ttu-id="e5030-126">A titok egységes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5030-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: Uri
Parameter Sets: SetByHostNameAndPort
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5030-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5030-127">CommonParameters</span></span>
<span data-ttu-id="e5030-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5030-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5030-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5030-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5030-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5030-130">INPUTS</span></span>

### <span data-ttu-id="e5030-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5030-131">None</span></span>
<span data-ttu-id="e5030-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e5030-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5030-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5030-133">OUTPUTS</span></span>

### <span data-ttu-id="e5030-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5030-134">None</span></span>

## <span data-ttu-id="e5030-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5030-135">NOTES</span></span>

## <span data-ttu-id="e5030-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5030-136">RELATED LINKS</span></span>

[<span data-ttu-id="e5030-137">Új – AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e5030-137">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="e5030-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e5030-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


