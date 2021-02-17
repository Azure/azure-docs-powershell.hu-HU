---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207798"
---
# <span data-ttu-id="a8acb-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8acb-101">New-AzStorageContext</span></span>

## <span data-ttu-id="a8acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8acb-102">SYNOPSIS</span></span>
<span data-ttu-id="a8acb-103">Azure-tárterület környezetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a8acb-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="a8acb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8acb-104">SYNTAX</span></span>

### <span data-ttu-id="a8acb-105">OAuthAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8acb-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8acb-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="a8acb-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8acb-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="a8acb-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="a8acb-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="a8acb-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8acb-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="a8acb-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="a8acb-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="a8acb-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8acb-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a8acb-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="a8acb-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="a8acb-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="a8acb-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a8acb-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="a8acb-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="a8acb-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="a8acb-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8acb-115">DESCRIPTION</span></span>
<span data-ttu-id="a8acb-116">A **New-AzStorageContext** parancsmag létrehoz egy Azure Storage környezetet.</span><span class="sxs-lookup"><span data-stu-id="a8acb-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="a8acb-117">A tárolási környezet alapértelmezett hitelesítése az OAuth (Azure AD), ha csak bemeneti tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="a8acb-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="a8acb-118">A társzolgáltatás hitelesítésének részleteit itt https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services olvashatja.</span><span class="sxs-lookup"><span data-stu-id="a8acb-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="a8acb-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8acb-119">EXAMPLES</span></span>

### <span data-ttu-id="a8acb-120">1. példa: Környezet létrehozása tárfiók nevének és kulcsának megadásával</span><span class="sxs-lookup"><span data-stu-id="a8acb-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="a8acb-121">Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="a8acb-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a8acb-122">2. példa: Környezet létrehozása kapcsolati karakterlánc megadásával</span><span class="sxs-lookup"><span data-stu-id="a8acb-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="a8acb-123">Ez a parancs a ContosoGeneral fiókhoz megadott kapcsolati karakterlánc alapján hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="a8acb-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="a8acb-124">3. példa: Környezet létrehozása névtelen tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="a8acb-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="a8acb-125">Ez a parancs kontextust hoz létre névtelen használatra a ContosoGeneral nevű fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a8acb-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="a8acb-126">A parancs a HTTP protokollt adja meg kapcsolati protokollként.</span><span class="sxs-lookup"><span data-stu-id="a8acb-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="a8acb-127">4. példa: Környezet létrehozása a helyi fejlesztési tárfiók használatával</span><span class="sxs-lookup"><span data-stu-id="a8acb-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="a8acb-128">Ez a parancs a helyi fejlesztési tárfiók használatával hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="a8acb-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="a8acb-129">A parancs a *Helyi paramétert adja* meg.</span><span class="sxs-lookup"><span data-stu-id="a8acb-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="a8acb-130">5. példa: A helyi fejlesztői tárfiók tárolója</span><span class="sxs-lookup"><span data-stu-id="a8acb-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="a8acb-131">Ez a parancs a helyi fejlesztési tárfiók használatával létrehoz egy környezetet, majd átadja az új környezetnek a **Get-AzStorageContainer** parancsmagot a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="a8acb-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a8acb-132">A parancs a helyi fejlesztői tárfiók Azure Storage tárolóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8acb-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="a8acb-133">6. példa: Több tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="a8acb-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="a8acb-134">Az első parancs a helyi fejlesztési tárfiók használatával létrehoz egy környezetet, majd ezt a környezetet a $Context 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8acb-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="a8acb-135">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd ezt a kontextust a $Context 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8acb-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="a8acb-136">Az utolsó parancs a $Context 01-ben és a $Context 02-ben a **Get-AzStorageContainer** használatával tárolt környezetek tárolóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8acb-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="a8acb-137">7. példa: Környezet létrehozása végponttal</span><span class="sxs-lookup"><span data-stu-id="a8acb-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="a8acb-138">Ez a parancs létrehoz egy Azure Storage környezetet, amely a megadott tárolási végponttal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="a8acb-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="a8acb-139">A parancs létrehozza a megadott kulcsot használó ContosoGeneral nevű fiók környezetét.</span><span class="sxs-lookup"><span data-stu-id="a8acb-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a8acb-140">8. példa: Környezet létrehozása egy adott környezetben</span><span class="sxs-lookup"><span data-stu-id="a8acb-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="a8acb-141">Ez a parancs létrehoz egy Azure-tárterületkörnyezetet, amely a megadott Azure-környezettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="a8acb-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="a8acb-142">A parancs létrehozza a megadott kulcsot használó ContosoGeneral nevű fiók környezetét.</span><span class="sxs-lookup"><span data-stu-id="a8acb-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="a8acb-143">9. példa: Környezet létrehozása SAS-jogkivonat használatával</span><span class="sxs-lookup"><span data-stu-id="a8acb-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="a8acb-144">Az első parancs egy SAS-jogkivonatot hoz létre a ContosoMain nevű tároló **New-AzStorageContainerSASToken** parancsmagját használva, majd a tokent a $SasToken változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8acb-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="a8acb-145">Ez a jogkivonat olvasási, hozzáadási, frissítési és törlési engedélyekhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="a8acb-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="a8acb-146">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a $SasToken-ban tárolt SAS-jogkivonatot használja, majd a környezet a $Context változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8acb-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="a8acb-147">A végleges parancs felsorolja a ContosoMain nevű tárolóhoz társított összes blobot a $Context.</span><span class="sxs-lookup"><span data-stu-id="a8acb-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="a8acb-148">10. példa: Környezet létrehozása OAuth-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="a8acb-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="a8acb-149">Ez a parancs az OAuth (Azure AD) hitelesítéssel hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="a8acb-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="a8acb-150">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8acb-150">PARAMETERS</span></span>

### <span data-ttu-id="a8acb-151">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="a8acb-151">-Anonymous</span></span>
<span data-ttu-id="a8acb-152">Azt jelzi, hogy ez a parancsmag létrehoz egy Azure Storage környezetet a névtelen bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="a8acb-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="a8acb-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a8acb-153">-ConnectionString</span></span>
<span data-ttu-id="a8acb-154">Egy kapcsolati karakterláncot ad meg az Azure Storage környezethez.</span><span class="sxs-lookup"><span data-stu-id="a8acb-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="a8acb-155">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="a8acb-155">-Endpoint</span></span>
<span data-ttu-id="a8acb-156">Az Azure Storage környezet végpontját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a8acb-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="a8acb-157">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a8acb-157">-Environment</span></span>
<span data-ttu-id="a8acb-158">Az Azure-környezetet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a8acb-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="a8acb-159">A paraméter elfogadható értékei: AzureCloud és AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="a8acb-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="a8acb-160">További információért írja be a `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="a8acb-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="a8acb-161">-Local</span><span class="sxs-lookup"><span data-stu-id="a8acb-161">-Local</span></span>
<span data-ttu-id="a8acb-162">Azt jelzi, hogy ez a parancsmag környezetet hoz létre a helyi fejlesztési tárfiók használatával.</span><span class="sxs-lookup"><span data-stu-id="a8acb-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="a8acb-163">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a8acb-163">-Protocol</span></span>
<span data-ttu-id="a8acb-164">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="a8acb-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="a8acb-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="a8acb-165">-SasToken</span></span>
<span data-ttu-id="a8acb-166">Egy SAS-jogkivonatot ad meg a környezethez.</span><span class="sxs-lookup"><span data-stu-id="a8acb-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="a8acb-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a8acb-167">-StorageAccountKey</span></span>
<span data-ttu-id="a8acb-168">Egy Azure Storage-fiókkulcsot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a8acb-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="a8acb-169">Ez a parancsmag a paraméter által megadott kulcs környezetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a8acb-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8acb-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a8acb-170">-StorageAccountName</span></span>
<span data-ttu-id="a8acb-171">Egy Azure Storage-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8acb-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="a8acb-172">Ez a parancsmag kontextust hoz létre a paraméter által megadott fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a8acb-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8acb-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="a8acb-173">-UseConnectedAccount</span></span>
<span data-ttu-id="a8acb-174">Azt jelzi, hogy ez a parancsmag Azure Storage környezetben hoz létre OAuth (Azure AD) hitelesítéssel.</span><span class="sxs-lookup"><span data-stu-id="a8acb-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="a8acb-175">A parancsmag alapértelmezés szerint OAuth-hitelesítést fog használni, ha más hitelesítés nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="a8acb-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

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

### <span data-ttu-id="a8acb-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8acb-176">CommonParameters</span></span>
<span data-ttu-id="a8acb-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8acb-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8acb-178">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8acb-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8acb-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8acb-179">INPUTS</span></span>

### <span data-ttu-id="a8acb-180">System.String</span><span class="sxs-lookup"><span data-stu-id="a8acb-180">System.String</span></span>

## <span data-ttu-id="a8acb-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8acb-181">OUTPUTS</span></span>

### <span data-ttu-id="a8acb-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8acb-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="a8acb-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8acb-183">NOTES</span></span>

## <span data-ttu-id="a8acb-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8acb-184">RELATED LINKS</span></span>

[<span data-ttu-id="a8acb-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a8acb-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a8acb-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a8acb-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


