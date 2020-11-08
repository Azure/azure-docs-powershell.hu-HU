---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024449"
---
# <span data-ttu-id="880c2-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="880c2-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="880c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="880c2-102">SYNOPSIS</span></span>
<span data-ttu-id="880c2-103">Adjon hozzá titkos tanúsítványt a csomópont típusához.</span><span class="sxs-lookup"><span data-stu-id="880c2-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="880c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="880c2-104">SYNTAX</span></span>

### <span data-ttu-id="880c2-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="880c2-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="880c2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="880c2-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="880c2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="880c2-107">DESCRIPTION</span></span>
<span data-ttu-id="880c2-108">Adjon hozzá titkos tanúsítványt a csomópont típusához.</span><span class="sxs-lookup"><span data-stu-id="880c2-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="880c2-109">A titkot az Azure Key Vault-ban kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="880c2-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="880c2-110">A Key Vault-ról további információt a mi az Azure Key Vault? című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="880c2-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="880c2-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="880c2-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="880c2-112">A parancsmagokról további információt az Azure Key Vault-parancsmagok ( https://msdn.microsoft.com/library/azure/dn868052.aspx) a Microsoft Developer Network Library vagy a Set-AzKeyVaultSecret parancsmag) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="880c2-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="880c2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="880c2-113">EXAMPLES</span></span>

### <span data-ttu-id="880c2-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="880c2-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="880c2-115">Ezzel a vesszővel elválasztott tanúsítvány titkos kulccsal, és a megadott titkos azonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="880c2-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="880c2-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="880c2-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="880c2-117">Ezzel a vesszővel elválasztott tanúsítvány titkos kulccsal rendelkezik, és a megadott titkos azonosítóval rendelkezik, a csövekkel.</span><span class="sxs-lookup"><span data-stu-id="880c2-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="880c2-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="880c2-118">PARAMETERS</span></span>

### <span data-ttu-id="880c2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="880c2-119">-AsJob</span></span>
<span data-ttu-id="880c2-120">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="880c2-120">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="880c2-121">-CertificateStore</span></span>
<span data-ttu-id="880c2-122">Annak a virtuális gépnek a tanúsítványtárolóját adja meg, amelyhez a tanúsítványt hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="880c2-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="880c2-123">A megadott tanúsítványtároló implicit módon szerepel az LocalMachine-fiókban.</span><span class="sxs-lookup"><span data-stu-id="880c2-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="880c2-124">-CertificateUrl</span></span>
<span data-ttu-id="880c2-125">Ez egy titkos kulcsként feltöltött tanúsítvány URL-címe.</span><span class="sxs-lookup"><span data-stu-id="880c2-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="880c2-126">Ha titkos kulcsot szeretne hozzáadni a kulcshoz, olvassa el a \[ kulcs vagy titok hozzáadása a kulcs boltozatához című témakört \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="880c2-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="880c2-127">Ebben az esetben a tanúsítványnak a következő JSON-objektum Base64-kódolásának kell lennie, amely UTF-8-ban kódolt: \<br\> \<br\> { \<br\> "Data": " \<Base64-encoded-certificate\> "; \<br\> "adattípus": "pfx", " \<br\> Password": " \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="880c2-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-128">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="880c2-128">-ClusterName</span></span>
<span data-ttu-id="880c2-129">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="880c2-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880c2-130">-DefaultProfile</span></span>
<span data-ttu-id="880c2-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="880c2-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="880c2-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="880c2-132">-InputObject</span></span>
<span data-ttu-id="880c2-133">Csomópont típusa erőforrás</span><span class="sxs-lookup"><span data-stu-id="880c2-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="880c2-134">-Name</span></span>
<span data-ttu-id="880c2-135">Adja meg a csomópont típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="880c2-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880c2-136">-ResourceGroupName</span></span>
<span data-ttu-id="880c2-137">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="880c2-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="880c2-138">-SourceVaultId</span></span>
<span data-ttu-id="880c2-139">A tanúsítványokat tartalmazó fő Vault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="880c2-139">Key Vault resource id containing the certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="880c2-140">-Confirm</span></span>
<span data-ttu-id="880c2-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="880c2-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="880c2-142">-WhatIf</span></span>
<span data-ttu-id="880c2-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="880c2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="880c2-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="880c2-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880c2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880c2-145">CommonParameters</span></span>
<span data-ttu-id="880c2-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="880c2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880c2-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="880c2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880c2-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="880c2-148">INPUTS</span></span>

### <span data-ttu-id="880c2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="880c2-149">System.String</span></span>

## <span data-ttu-id="880c2-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="880c2-150">OUTPUTS</span></span>

### <span data-ttu-id="880c2-151">Microsoft. Azure. Command. ServiceFabric. models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="880c2-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="880c2-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="880c2-152">NOTES</span></span>

## <span data-ttu-id="880c2-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="880c2-153">RELATED LINKS</span></span>
