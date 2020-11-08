---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187168"
---
# <span data-ttu-id="1ad6c-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ad6c-101">New-AzStorageContext</span></span>

## <span data-ttu-id="1ad6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ad6c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad6c-103">Azure-tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="1ad6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ad6c-104">SYNTAX</span></span>

### <span data-ttu-id="1ad6c-105">OAuthAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ad6c-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="1ad6c-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="1ad6c-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6c-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="1ad6c-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="1ad6c-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1ad6c-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="1ad6c-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ad6c-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="1ad6c-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="1ad6c-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="1ad6c-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ad6c-115">DESCRIPTION</span></span>
<span data-ttu-id="1ad6c-116">A **New-AzStorageContext** parancsmag Azure-tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="1ad6c-117">A tárolási környezet alapértelmezett hitelesítése a OAuth (Azure AD), ha csak az adattárolási fiók neve látható.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="1ad6c-118">Tekintse meg a tárolási szolgáltatás hitelesítésének részleteit https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="1ad6c-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="1ad6c-119">Példák</span><span class="sxs-lookup"><span data-stu-id="1ad6c-119">EXAMPLES</span></span>

### <span data-ttu-id="1ad6c-120">Példa 1: környezet létrehozása tárolási fiók nevének és kulcsának megadásával</span><span class="sxs-lookup"><span data-stu-id="1ad6c-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="1ad6c-121">Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="1ad6c-122">2. példa: környezet létrehozása kapcsolati karakterlánc megadásával</span><span class="sxs-lookup"><span data-stu-id="1ad6c-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="1ad6c-123">A parancs a megadott kapcsolati karakterláncon alapuló környezetet hoz létre a fiók ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="1ad6c-124">Példa 3: névtelen tárterület-fiók környezetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="1ad6c-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="1ad6c-125">Ez a parancs a ContosoGeneral nevű fiók névtelen használatára szolgáló környezetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="1ad6c-126">A parancs a HTTP protokollt adja meg kapcsolati protokollként.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="1ad6c-127">Példa 4: környezet létrehozása a helyi fejlesztési tárterület-fiók használatával</span><span class="sxs-lookup"><span data-stu-id="1ad6c-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="1ad6c-128">A parancs a helyi fejlesztési tárterület-fiók segítségével hozza létre a környezetet.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="1ad6c-129">A parancs a *helyi* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="1ad6c-130">Példa 5: a helyi fejlesztői tárterület-fiók tárolójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="1ad6c-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="1ad6c-131">A parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd átadja az új környezetet a **Get-AzStorageContainer** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1ad6c-132">A parancs az Azure Storage containert kapja meg a helyi fejlesztői tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="1ad6c-133">Példa 6: több tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="1ad6c-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="1ad6c-134">Az első parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd a $Context 01 változóban tárolja ezt a környezetet.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="1ad6c-135">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a környezetet a $Context 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="1ad6c-136">A végleges parancs a **Get-AzStorageContainer** a $Context 01-ben és a $Context 02-ban tárolt környezetek tárolóit kapja.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="1ad6c-137">7. példa: környezet létrehozása végponttal</span><span class="sxs-lookup"><span data-stu-id="1ad6c-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="1ad6c-138">A parancs létrehoz egy Azure-tárterületet, amely a megadott tárterület-végponttal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="1ad6c-139">A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="1ad6c-140">8. példa: környezet létrehozása meghatározott környezettel</span><span class="sxs-lookup"><span data-stu-id="1ad6c-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="1ad6c-141">Ez a parancs olyan Azure-tárterületet hoz létre, amely a megadott Azure-környezettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="1ad6c-142">A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="1ad6c-143">Példa 9: környezet létrehozása SAS-token használatával</span><span class="sxs-lookup"><span data-stu-id="1ad6c-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="1ad6c-144">Az első parancs a ContosoMain nevű tároló **új-AzStorageContainerSASToken** parancsmagjának segítségével hoz létre egy sas-tokent, majd a tokent a $SasToken változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="1ad6c-145">Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="1ad6c-146">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a $SasTokenban tárolt SAS-jogkivonatot használja, majd a $Context változóban tárolja ezt a környezetet.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="1ad6c-147">A végleges parancs felsorolja a ContosoMain nevű tárolóhoz társított összes blobot az $Context-ben tárolt környezettel.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="1ad6c-148">10. példa: környezet létrehozása a OAuth-hitelesítés használatával</span><span class="sxs-lookup"><span data-stu-id="1ad6c-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="1ad6c-149">Ez a parancs a OAuth (Azure AD) hitelesítés használatával hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="1ad6c-150">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ad6c-150">PARAMETERS</span></span>

### <span data-ttu-id="1ad6c-151">-Névtelen</span><span class="sxs-lookup"><span data-stu-id="1ad6c-151">-Anonymous</span></span>
<span data-ttu-id="1ad6c-152">Jelzi, hogy ez a parancsmag Azure-tárterületet hoz létre a névtelen bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="1ad6c-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ad6c-153">-ConnectionString</span></span>
<span data-ttu-id="1ad6c-154">Az Azure tárolási környezet kapcsolati karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="1ad6c-155">-Végpont</span><span class="sxs-lookup"><span data-stu-id="1ad6c-155">-Endpoint</span></span>
<span data-ttu-id="1ad6c-156">Az Azure tárolási környezet végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="1ad6c-157">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1ad6c-157">-Environment</span></span>
<span data-ttu-id="1ad6c-158">Az Azure-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="1ad6c-159">A paraméter elfogadható értékei a következők: AzureCloud és AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="1ad6c-160">További információért írja be a következőt: `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="1ad6c-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="1ad6c-161">-Local (helyi)</span><span class="sxs-lookup"><span data-stu-id="1ad6c-161">-Local</span></span>
<span data-ttu-id="1ad6c-162">Jelzi, hogy a parancsmag a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="1ad6c-163">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1ad6c-163">-Protocol</span></span>
<span data-ttu-id="1ad6c-164">Átviteli protokoll (https/http).</span><span class="sxs-lookup"><span data-stu-id="1ad6c-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="1ad6c-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="1ad6c-165">-SasToken</span></span>
<span data-ttu-id="1ad6c-166">Egy megosztott hozzáférés-aláírási (SAS) tokent ad meg a kontextushoz.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="1ad6c-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1ad6c-167">-StorageAccountKey</span></span>
<span data-ttu-id="1ad6c-168">Az Azure Storage Account kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="1ad6c-169">Ez a parancsmag létrehoz egy környezetet annak a kulcsnak, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ad6c-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1ad6c-170">-StorageAccountName</span></span>
<span data-ttu-id="1ad6c-171">Az Azure Storage-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="1ad6c-172">Ez a parancsmag a paraméter által megadott fiók környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ad6c-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6c-173">-UseConnectedAccount</span></span>
<span data-ttu-id="1ad6c-174">Jelzi, hogy ez a parancsmag Azure-tárterületet hoz létre a OAuth (Azure AD) hitelesítéssel.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="1ad6c-175">A parancsmag alapértelmezés szerint a OAuth-hitelesítést fogja használni, ha más hitelesítés nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="1ad6c-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

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

### <span data-ttu-id="1ad6c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad6c-176">CommonParameters</span></span>
<span data-ttu-id="1ad6c-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ad6c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad6c-178">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad6c-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad6c-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad6c-179">INPUTS</span></span>

### <span data-ttu-id="1ad6c-180">System. String</span><span class="sxs-lookup"><span data-stu-id="1ad6c-180">System.String</span></span>

## <span data-ttu-id="1ad6c-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad6c-181">OUTPUTS</span></span>

### <span data-ttu-id="1ad6c-182">Microsoft. WindowsAzure. Command. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ad6c-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="1ad6c-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ad6c-183">NOTES</span></span>

## <span data-ttu-id="1ad6c-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ad6c-184">RELATED LINKS</span></span>

[<span data-ttu-id="1ad6c-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1ad6c-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="1ad6c-186">Új – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="1ad6c-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


