---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e807d1fd1c630554bbaefe0cae1dd225b5f1a184
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679480"
---
# <span data-ttu-id="1b124-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="1b124-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="1b124-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b124-102">SYNOPSIS</span></span>
<span data-ttu-id="1b124-103">Módosította az adattó-statisztika-katalógus titkát.</span><span class="sxs-lookup"><span data-stu-id="1b124-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b124-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b124-104">SYNTAX</span></span>

### <span data-ttu-id="1b124-105">Teljes URI megadása</span><span class="sxs-lookup"><span data-stu-id="1b124-105">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b124-106">Az állomás nevének és portjának megadása</span><span class="sxs-lookup"><span data-stu-id="1b124-106">Specify host name and port</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b124-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b124-107">DESCRIPTION</span></span>
<span data-ttu-id="1b124-108">A **set-AzureRmDataLakeAnalyticsCatalogSecret** parancsmag módosította az Azure Data Lake-Lake Analytics-katalógushoz társított titkot.</span><span class="sxs-lookup"><span data-stu-id="1b124-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="1b124-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1b124-109">EXAMPLES</span></span>

### <span data-ttu-id="1b124-110">Példa 1: egy fiókkal társított titok módosítása</span><span class="sxs-lookup"><span data-stu-id="1b124-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="1b124-111">Ez a parancs a Data Lake Analytics-katalógushoz társított titkot állítja be.</span><span class="sxs-lookup"><span data-stu-id="1b124-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="1b124-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b124-112">PARAMETERS</span></span>

### <span data-ttu-id="1b124-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="1b124-113">-Account</span></span>
<span data-ttu-id="1b124-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b124-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1b124-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="1b124-115">-DatabaseHost</span></span>
<span data-ttu-id="1b124-116">Annak az adatbázisnak az állomásnevét adja meg, amelynek a titka az "mydatabase.contoso.com" formátumban van társítva.</span><span class="sxs-lookup"><span data-stu-id="1b124-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b124-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b124-117">-DatabaseName</span></span>
<span data-ttu-id="1b124-118">A titkot birtokló adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b124-118">Specifies the name of the database holding the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b124-119">-Port</span><span class="sxs-lookup"><span data-stu-id="1b124-119">-Port</span></span>
<span data-ttu-id="1b124-120">A titok portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b124-120">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b124-121">-Secret</span><span class="sxs-lookup"><span data-stu-id="1b124-121">-Secret</span></span>
<span data-ttu-id="1b124-122">A titok nevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b124-122">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b124-123">-URI</span><span class="sxs-lookup"><span data-stu-id="1b124-123">-Uri</span></span>
<span data-ttu-id="1b124-124">A titok egységes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b124-124">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b124-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b124-125">-DefaultProfile</span></span>
<span data-ttu-id="1b124-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b124-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b124-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b124-127">CommonParameters</span></span>
<span data-ttu-id="1b124-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b124-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b124-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b124-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b124-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b124-130">INPUTS</span></span>

## <span data-ttu-id="1b124-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b124-131">OUTPUTS</span></span>

### <span data-ttu-id="1b124-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="1b124-132">None</span></span>

## <span data-ttu-id="1b124-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b124-133">NOTES</span></span>

## <span data-ttu-id="1b124-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b124-134">RELATED LINKS</span></span>

[<span data-ttu-id="1b124-135">Új – AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="1b124-135">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="1b124-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="1b124-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


