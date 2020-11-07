---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
ms.openlocfilehash: 3a91c88fe80151ef8aa3934c484cfe9b6671a750
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849826"
---
# <span data-ttu-id="0d65a-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0d65a-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="0d65a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d65a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d65a-103">Azure-tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0d65a-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d65a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d65a-104">SYNTAX</span></span>

### <span data-ttu-id="0d65a-105">AccountNameAndKey (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d65a-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d65a-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="0d65a-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="0d65a-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="0d65a-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d65a-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="0d65a-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="0d65a-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="0d65a-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d65a-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0d65a-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="0d65a-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0d65a-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="0d65a-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="0d65a-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="0d65a-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d65a-113">DESCRIPTION</span></span>
<span data-ttu-id="0d65a-114">A **New-AzureStorageContext** parancsmag Azure-tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0d65a-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="0d65a-115">Példák</span><span class="sxs-lookup"><span data-stu-id="0d65a-115">EXAMPLES</span></span>

### <span data-ttu-id="0d65a-116">Példa 1: környezet létrehozása tárolási fiók nevének és kulcsának megadásával</span><span class="sxs-lookup"><span data-stu-id="0d65a-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="0d65a-117">Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="0d65a-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="0d65a-118">2. példa: környezet létrehozása kapcsolati karakterlánc megadásával</span><span class="sxs-lookup"><span data-stu-id="0d65a-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="0d65a-119">A parancs a megadott kapcsolati karakterláncon alapuló környezetet hoz létre a fiók ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="0d65a-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="0d65a-120">Példa 3: névtelen tárterület-fiók környezetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="0d65a-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="0d65a-121">Ez a parancs a ContosoGeneral nevű fiók névtelen használatára szolgáló környezetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0d65a-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="0d65a-122">A parancs a HTTP protokollt adja meg kapcsolati protokollként.</span><span class="sxs-lookup"><span data-stu-id="0d65a-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="0d65a-123">Példa 4: környezet létrehozása a helyi fejlesztési tárterület-fiók használatával</span><span class="sxs-lookup"><span data-stu-id="0d65a-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="0d65a-124">A parancs a helyi fejlesztési tárterület-fiók segítségével hozza létre a környezetet.</span><span class="sxs-lookup"><span data-stu-id="0d65a-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="0d65a-125">A parancs a *helyi* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d65a-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="0d65a-126">Példa 5: a helyi fejlesztői tárterület-fiók tárolójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d65a-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="0d65a-127">A parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd átadja az új környezetet a **Get-AzureStorageContainer** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="0d65a-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d65a-128">A parancs az Azure Storage containert kapja meg a helyi fejlesztői tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="0d65a-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="0d65a-129">Példa 6: több tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d65a-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="0d65a-130">Az első parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd a $Context 01 változóban tárolja ezt a környezetet.</span><span class="sxs-lookup"><span data-stu-id="0d65a-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="0d65a-131">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a környezetet a $Context 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d65a-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="0d65a-132">A végleges parancs a **Get-AzureStorageContainer** a $Context 01-ben és a $Context 02-ban tárolt környezetek tárolóit kapja.</span><span class="sxs-lookup"><span data-stu-id="0d65a-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="0d65a-133">7. példa: környezet létrehozása végponttal</span><span class="sxs-lookup"><span data-stu-id="0d65a-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="0d65a-134">A parancs létrehoz egy Azure-tárterületet, amely a megadott tárterület-végponttal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="0d65a-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="0d65a-135">A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="0d65a-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="0d65a-136">8. példa: környezet létrehozása meghatározott környezettel</span><span class="sxs-lookup"><span data-stu-id="0d65a-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="0d65a-137">Ez a parancs olyan Azure-tárterületet hoz létre, amely a megadott Azure-környezettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="0d65a-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="0d65a-138">A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="0d65a-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="0d65a-139">Példa 9: környezet létrehozása SAS-token használatával</span><span class="sxs-lookup"><span data-stu-id="0d65a-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="0d65a-140">Az első parancs a ContosoMain nevű tároló **új-AzureStorageContainerSASToken** parancsmagjának segítségével hoz létre egy sas-tokent, majd a tokent a $SasToken változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d65a-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="0d65a-141">Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.</span><span class="sxs-lookup"><span data-stu-id="0d65a-141">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="0d65a-142">A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a $SasTokenban tárolt SAS-jogkivonatot használja, majd a $Context változóban tárolja ezt a környezetet.</span><span class="sxs-lookup"><span data-stu-id="0d65a-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="0d65a-143">A végleges parancs felsorolja a ContosoMain nevű tárolóhoz társított összes blobot az $Context-ben tárolt környezettel.</span><span class="sxs-lookup"><span data-stu-id="0d65a-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="0d65a-144">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d65a-144">PARAMETERS</span></span>

### <span data-ttu-id="0d65a-145">-Névtelen</span><span class="sxs-lookup"><span data-stu-id="0d65a-145">-Anonymous</span></span>
<span data-ttu-id="0d65a-146">Jelzi, hogy ez a parancsmag Azure-tárterületet hoz létre a névtelen bejelentkezéshez.</span><span class="sxs-lookup"><span data-stu-id="0d65a-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="0d65a-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0d65a-147">-ConnectionString</span></span>
<span data-ttu-id="0d65a-148">Az Azure tárolási környezet kapcsolati karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d65a-148">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="0d65a-149">-Végpont</span><span class="sxs-lookup"><span data-stu-id="0d65a-149">-Endpoint</span></span>
<span data-ttu-id="0d65a-150">Az Azure tárolási környezet végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d65a-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d65a-151">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0d65a-151">-Environment</span></span>
<span data-ttu-id="0d65a-152">Az Azure-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d65a-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="0d65a-153">A paraméter elfogadható értékei a következők: AzureCloud és AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="0d65a-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="0d65a-154">További információért írja be a következőt: `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="0d65a-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

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
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d65a-155">-Local (helyi)</span><span class="sxs-lookup"><span data-stu-id="0d65a-155">-Local</span></span>
<span data-ttu-id="0d65a-156">Jelzi, hogy a parancsmag a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet.</span><span class="sxs-lookup"><span data-stu-id="0d65a-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="0d65a-157">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0d65a-157">-Protocol</span></span>
<span data-ttu-id="0d65a-158">Átviteli protokoll (https/http).</span><span class="sxs-lookup"><span data-stu-id="0d65a-158">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d65a-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="0d65a-159">-SasToken</span></span>
<span data-ttu-id="0d65a-160">Egy megosztott hozzáférés-aláírási (SAS) tokent ad meg a kontextushoz.</span><span class="sxs-lookup"><span data-stu-id="0d65a-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="0d65a-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0d65a-161">-StorageAccountKey</span></span>
<span data-ttu-id="0d65a-162">Az Azure Storage Account kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d65a-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="0d65a-163">Ez a parancsmag létrehoz egy környezetet annak a kulcsnak, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="0d65a-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="0d65a-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0d65a-164">-StorageAccountName</span></span>
<span data-ttu-id="0d65a-165">Az Azure Storage-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d65a-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="0d65a-166">Ez a parancsmag a paraméter által megadott fiók környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d65a-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d65a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d65a-167">CommonParameters</span></span>
<span data-ttu-id="0d65a-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d65a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d65a-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d65a-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d65a-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d65a-170">INPUTS</span></span>

### <span data-ttu-id="0d65a-171">System. String</span><span class="sxs-lookup"><span data-stu-id="0d65a-171">System.String</span></span>

## <span data-ttu-id="0d65a-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d65a-172">OUTPUTS</span></span>

### <span data-ttu-id="0d65a-173">Microsoft. WindowsAzure. Command. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0d65a-173">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="0d65a-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d65a-174">NOTES</span></span>

## <span data-ttu-id="0d65a-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d65a-175">RELATED LINKS</span></span>

[<span data-ttu-id="0d65a-176">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0d65a-176">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="0d65a-177">Új – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0d65a-177">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


