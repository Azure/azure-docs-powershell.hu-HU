---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
gitcommit: https://github.com/Azure/azure-powershell/blob/89262bc4144696c69376c3fb654c881de55b6450
ms.openlocfilehash: 2e9d3689a29a54f7af873cd1a11fdbc343509eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680789"
---
# <span data-ttu-id="abcab-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="abcab-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="abcab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abcab-102">SYNOPSIS</span></span>
<span data-ttu-id="abcab-103">Azure-tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="abcab-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abcab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abcab-104">SYNTAX</span></span>

### <span data-ttu-id="abcab-105">AccountNameAndKey (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abcab-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="abcab-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="abcab-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="abcab-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="abcab-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="abcab-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="abcab-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="abcab-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="abcab-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="abcab-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="abcab-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="abcab-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="abcab-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="abcab-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="abcab-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="abcab-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="abcab-113">DESCRIPTION</span></span>
<span data-ttu-id="abcab-114">A **New-AzureStorageContext** parancsmag Azure-tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="abcab-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="abcab-115">Példák</span><span class="sxs-lookup"><span data-stu-id="abcab-115">EXAMPLES</span></span>

### <span data-ttu-id="abcab-116">Példa 1: környezet létrehozása tárolási fiók nevének és kulcsának megadásával</span><span class="sxs-lookup"><span data-stu-id="abcab-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="abcab-117">Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="abcab-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="abcab-118">2. példa: környezet létrehozása kapcsolati karakterlánc megadásával</span><span class="sxs-lookup"><span data-stu-id="abcab-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="abcab-119">A parancs a megadott kapcsolati karakterláncon alapuló környezetet hoz létre a fiók ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="abcab-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="abcab-120">Példa 3: névtelen tárterület-fiók környezetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="abcab-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="abcab-121">Ez a parancs a ContosoGeneral nevű fiók névtelen használatára szolgáló környezetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="abcab-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="abcab-122">A parancs a HTTP protokollt adja meg kapcsolati protokollként.</span><span class="sxs-lookup"><span data-stu-id="abcab-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="abcab-123">Példa 4: környezet létrehozása a helyi fejlesztési tárterület-fiók használatával</span><span class="sxs-lookup"><span data-stu-id="abcab-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="abcab-124">A parancs a helyi fejlesztési tárterület-fiók segítségével hozza létre a környezetet.</span><span class="sxs-lookup"><span data-stu-id="abcab-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="abcab-125">A parancs a *helyi* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcab-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="abcab-126">Példa 5: a helyi fejlesztői tárterület-fiók tárolójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="abcab-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="abcab-127">A parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd átadja az új környezetet a **Get-AzureStorageContainer** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="abcab-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="abcab-128">A parancs az Azure Storage containert kapja meg a helyi fejlesztői tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="abcab-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="abcab-129">Példa 6: több tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="abcab-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="abcab-130">Az első parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd a $Context 01 változóban tárolja ezt a környezetet.</span><span class="sxs-lookup"><span data-stu-id="abcab-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>

<span data-ttu-id="abcab-131">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a környezetet a $Context 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="abcab-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>

<span data-ttu-id="abcab-132">A végleges parancs a **Get-AzureStorageContainer** a $Context 01-ben és a $Context 02-ban tárolt környezetek tárolóit kapja.</span><span class="sxs-lookup"><span data-stu-id="abcab-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="abcab-133">7. példa: környezet létrehozása végponttal</span><span class="sxs-lookup"><span data-stu-id="abcab-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="abcab-134">A parancs létrehoz egy Azure-tárterületet, amely a megadott tárterület-végponttal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="abcab-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="abcab-135">A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="abcab-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="abcab-136">8. példa: környezet létrehozása meghatározott környezettel</span><span class="sxs-lookup"><span data-stu-id="abcab-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="abcab-137">Ez a parancs olyan Azure-tárterületet hoz létre, amely a megadott Azure-környezettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="abcab-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="abcab-138">A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="abcab-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="abcab-139">Példa 9: környezet létrehozása SAS-token használatával</span><span class="sxs-lookup"><span data-stu-id="abcab-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="abcab-140">Az első parancs a ContosoMain nevű tároló **új-AzureStorageContainerSASToken** parancsmagjának segítségével hoz létre egy sas-tokent, majd a tokent a $SasToken változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="abcab-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="abcab-141">Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.</span><span class="sxs-lookup"><span data-stu-id="abcab-141">That token is for read, add, update, and delete permissions.</span></span>

<span data-ttu-id="abcab-142">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a $SasTokenban tárolt SAS-jogkivonatot használja, majd a $Context változóban tárolja ezt a környezetet.</span><span class="sxs-lookup"><span data-stu-id="abcab-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>

<span data-ttu-id="abcab-143">A végleges parancs felsorolja a ContosoMain nevű tárolóhoz társított összes blobot az $Context-ben tárolt környezettel.</span><span class="sxs-lookup"><span data-stu-id="abcab-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="abcab-144">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abcab-144">PARAMETERS</span></span>

### <span data-ttu-id="abcab-145">-Névtelen</span><span class="sxs-lookup"><span data-stu-id="abcab-145">-Anonymous</span></span>
<span data-ttu-id="abcab-146">Jelzi, hogy ez a parancsmag Azure-tárterületet hoz létre a névtelen bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="abcab-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="abcab-147">-ConnectionString</span></span>
<span data-ttu-id="abcab-148">Az Azure tárolási környezet kapcsolati karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcab-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-149">-Végpont</span><span class="sxs-lookup"><span data-stu-id="abcab-149">-Endpoint</span></span>
<span data-ttu-id="abcab-150">Az Azure tárolási környezet végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcab-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-151">-Környezet</span><span class="sxs-lookup"><span data-stu-id="abcab-151">-Environment</span></span>
<span data-ttu-id="abcab-152">Az Azure-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcab-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="abcab-153">A paraméter elfogadható értékei a következők: AzureCloud és AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="abcab-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="abcab-154">További információért írja be a következőt: `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="abcab-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-155">-Local (helyi)</span><span class="sxs-lookup"><span data-stu-id="abcab-155">-Local</span></span>
<span data-ttu-id="abcab-156">Jelzi, hogy a parancsmag a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="abcab-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-157">-Protocol</span><span class="sxs-lookup"><span data-stu-id="abcab-157">-Protocol</span></span>
<span data-ttu-id="abcab-158">Átviteli protokoll (https/http).</span><span class="sxs-lookup"><span data-stu-id="abcab-158">Transfer Protocol (https/http).</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="abcab-159">-SasToken</span></span>
<span data-ttu-id="abcab-160">Egy megosztott hozzáférés-aláírási (SAS) tokent ad meg a kontextushoz.</span><span class="sxs-lookup"><span data-stu-id="abcab-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="abcab-161">-StorageAccountKey</span></span>
<span data-ttu-id="abcab-162">Az Azure Storage Account kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcab-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="abcab-163">Ez a parancsmag létrehoz egy környezetet annak a kulcsnak, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="abcab-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="abcab-164">-StorageAccountName</span></span>
<span data-ttu-id="abcab-165">Az Azure Storage-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcab-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="abcab-166">Ez a parancsmag a paraméter által megadott fiók környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abcab-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcab-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcab-167">CommonParameters</span></span>
<span data-ttu-id="abcab-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abcab-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abcab-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abcab-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcab-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abcab-170">INPUTS</span></span>

## <span data-ttu-id="abcab-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abcab-171">OUTPUTS</span></span>

### <span data-ttu-id="abcab-172">AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="abcab-172">AzureStorageContext</span></span>

## <span data-ttu-id="abcab-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abcab-173">NOTES</span></span>

## <span data-ttu-id="abcab-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abcab-174">RELATED LINKS</span></span>

[<span data-ttu-id="abcab-175">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="abcab-175">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="abcab-176">Új – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="abcab-176">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


