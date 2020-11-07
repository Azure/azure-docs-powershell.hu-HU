---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: eca1322f1638039fce6c478b19e94b586fd83bbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839771"
---
# <span data-ttu-id="15808-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="15808-101">New-AzStorageContext</span></span>

## <span data-ttu-id="15808-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15808-102">SYNOPSIS</span></span>
<span data-ttu-id="15808-103">Azure-tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="15808-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="15808-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15808-104">SYNTAX</span></span>

### <span data-ttu-id="15808-105">OAuthAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15808-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="15808-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="15808-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="15808-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="15808-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="15808-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="15808-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="15808-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="15808-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="15808-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="15808-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="15808-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="15808-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="15808-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="15808-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="15808-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="15808-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="15808-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="15808-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="15808-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="15808-115">DESCRIPTION</span></span>
<span data-ttu-id="15808-116">A **New-AzStorageContext** parancsmag Azure-tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="15808-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="15808-117">A tárolási környezet alapértelmezett hitelesítése a OAuth (Azure AD), ha csak az adattárolási fiók neve látható.</span><span class="sxs-lookup"><span data-stu-id="15808-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="15808-118">Tekintse meg a tárolási szolgáltatás hitelesítésének részleteit https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="15808-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="15808-119">Példák</span><span class="sxs-lookup"><span data-stu-id="15808-119">EXAMPLES</span></span>

### <span data-ttu-id="15808-120">Példa 1: környezet létrehozása tárolási fiók nevének és kulcsának megadásával</span><span class="sxs-lookup"><span data-stu-id="15808-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="15808-121">Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="15808-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="15808-122">2. példa: környezet létrehozása kapcsolati karakterlánc megadásával</span><span class="sxs-lookup"><span data-stu-id="15808-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="15808-123">A parancs a megadott kapcsolati karakterláncon alapuló környezetet hoz létre a fiók ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="15808-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="15808-124">Példa 3: névtelen tárterület-fiók környezetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="15808-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="15808-125">Ez a parancs a ContosoGeneral nevű fiók névtelen használatára szolgáló környezetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="15808-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="15808-126">A parancs a HTTP protokollt adja meg kapcsolati protokollként.</span><span class="sxs-lookup"><span data-stu-id="15808-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="15808-127">Példa 4: környezet létrehozása a helyi fejlesztési tárterület-fiók használatával</span><span class="sxs-lookup"><span data-stu-id="15808-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="15808-128">A parancs a helyi fejlesztési tárterület-fiók segítségével hozza létre a környezetet.</span><span class="sxs-lookup"><span data-stu-id="15808-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="15808-129">A parancs a *helyi* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="15808-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="15808-130">Példa 5: a helyi fejlesztői tárterület-fiók tárolójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="15808-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="15808-131">A parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd átadja az új környezetet a **Get-AzStorageContainer** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="15808-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="15808-132">A parancs az Azure Storage containert kapja meg a helyi fejlesztői tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="15808-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="15808-133">Példa 6: több tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="15808-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="15808-134">Az első parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd a $Context 01 változóban tárolja ezt a környezetet.</span><span class="sxs-lookup"><span data-stu-id="15808-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="15808-135">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a környezetet a $Context 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15808-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="15808-136">A végleges parancs a **Get-AzStorageContainer** a $Context 01-ben és a $Context 02-ban tárolt környezetek tárolóit kapja.</span><span class="sxs-lookup"><span data-stu-id="15808-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="15808-137">7. példa: környezet létrehozása végponttal</span><span class="sxs-lookup"><span data-stu-id="15808-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="15808-138">A parancs létrehoz egy Azure-tárterületet, amely a megadott tárterület-végponttal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="15808-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="15808-139">A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="15808-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="15808-140">8. példa: környezet létrehozása meghatározott környezettel</span><span class="sxs-lookup"><span data-stu-id="15808-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="15808-141">Ez a parancs olyan Azure-tárterületet hoz létre, amely a megadott Azure-környezettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="15808-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="15808-142">A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="15808-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="15808-143">Példa 9: környezet létrehozása SAS-token használatával</span><span class="sxs-lookup"><span data-stu-id="15808-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="15808-144">Az első parancs a ContosoMain nevű tároló **új-AzStorageContainerSASToken** parancsmagjának segítségével hoz létre egy sas-tokent, majd a tokent a $SasToken változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15808-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="15808-145">Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.</span><span class="sxs-lookup"><span data-stu-id="15808-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="15808-146">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a $SasTokenban tárolt SAS-jogkivonatot használja, majd a $Context változóban tárolja ezt a környezetet.</span><span class="sxs-lookup"><span data-stu-id="15808-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="15808-147">A végleges parancs felsorolja a ContosoMain nevű tárolóhoz társított összes blobot az $Context-ben tárolt környezettel.</span><span class="sxs-lookup"><span data-stu-id="15808-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="15808-148">10. példa: környezet létrehozása a OAuth-hitelesítés használatával</span><span class="sxs-lookup"><span data-stu-id="15808-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="15808-149">Ez a parancs a OAuth (Azure AD) hitelesítés használatával hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="15808-149">This command creates a context by using the OAuth (Azure AD)  Authentication.</span></span>

## <span data-ttu-id="15808-150">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15808-150">PARAMETERS</span></span>

### <span data-ttu-id="15808-151">-Névtelen</span><span class="sxs-lookup"><span data-stu-id="15808-151">-Anonymous</span></span>
<span data-ttu-id="15808-152">Jelzi, hogy ez a parancsmag Azure-tárterületet hoz létre a névtelen bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="15808-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="15808-153">-ConnectionString</span></span>
<span data-ttu-id="15808-154">Az Azure tárolási környezet kapcsolati karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="15808-154">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-155">-Végpont</span><span class="sxs-lookup"><span data-stu-id="15808-155">-Endpoint</span></span>
<span data-ttu-id="15808-156">Az Azure tárolási környezet végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="15808-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-157">-Környezet</span><span class="sxs-lookup"><span data-stu-id="15808-157">-Environment</span></span>
<span data-ttu-id="15808-158">Az Azure-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="15808-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="15808-159">A paraméter elfogadható értékei a következők: AzureCloud és AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="15808-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="15808-160">További információért írja be a következőt: `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="15808-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15808-161">-Local (helyi)</span><span class="sxs-lookup"><span data-stu-id="15808-161">-Local</span></span>
<span data-ttu-id="15808-162">Jelzi, hogy a parancsmag a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="15808-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-163">-Protocol</span><span class="sxs-lookup"><span data-stu-id="15808-163">-Protocol</span></span>
<span data-ttu-id="15808-164">Átviteli protokoll (https/http).</span><span class="sxs-lookup"><span data-stu-id="15808-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="15808-165">-SasToken</span></span>
<span data-ttu-id="15808-166">Egy megosztott hozzáférés-aláírási (SAS) tokent ad meg a kontextushoz.</span><span class="sxs-lookup"><span data-stu-id="15808-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="15808-167">-StorageAccountKey</span></span>
<span data-ttu-id="15808-168">Az Azure Storage Account kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="15808-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="15808-169">Ez a parancsmag létrehoz egy környezetet annak a kulcsnak, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="15808-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="15808-170">-StorageAccountName</span></span>
<span data-ttu-id="15808-171">Az Azure Storage-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15808-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="15808-172">Ez a parancsmag a paraméter által megadott fiók környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15808-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="15808-173">-UseConnectedAccount</span></span>
<span data-ttu-id="15808-174">Jelzi, hogy ez a parancsmag Azure-tárterületet hoz létre a OAuth (Azure AD) hitelesítéssel.</span><span class="sxs-lookup"><span data-stu-id="15808-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="15808-175">A parancsmag alapértelmezés szerint a OAuth-hitelesítést fogja használni, ha más hitelesítés nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="15808-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15808-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15808-176">CommonParameters</span></span>
<span data-ttu-id="15808-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15808-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15808-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15808-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15808-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15808-179">INPUTS</span></span>

### <span data-ttu-id="15808-180">System. String</span><span class="sxs-lookup"><span data-stu-id="15808-180">System.String</span></span>

## <span data-ttu-id="15808-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15808-181">OUTPUTS</span></span>

### <span data-ttu-id="15808-182">Microsoft. WindowsAzure. Command. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="15808-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="15808-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15808-183">NOTES</span></span>

## <span data-ttu-id="15808-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15808-184">RELATED LINKS</span></span>

[<span data-ttu-id="15808-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="15808-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="15808-186">Új – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="15808-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


