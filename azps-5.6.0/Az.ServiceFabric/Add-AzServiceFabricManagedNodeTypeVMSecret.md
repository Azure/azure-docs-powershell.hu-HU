---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 35d755bc117ccc4379be8d7344d8e7170594d555
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927513"
---
# <span data-ttu-id="1929f-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="1929f-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="1929f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1929f-102">SYNOPSIS</span></span>
<span data-ttu-id="1929f-103">Adja hozzá a tanúsítvány titkos nevét a csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="1929f-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="1929f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1929f-104">SYNTAX</span></span>

### <span data-ttu-id="1929f-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1929f-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1929f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1929f-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1929f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1929f-107">DESCRIPTION</span></span>
<span data-ttu-id="1929f-108">Adja hozzá a tanúsítvány titkos nevét a csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="1929f-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="1929f-109">A titkos kulcsot egy Azure-kulcstárolóban kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="1929f-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="1929f-110">A kulcstárra vonatkozó további információkért lásd: Mi az Azure-kulcstár?</span><span class="sxs-lookup"><span data-stu-id="1929f-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="1929f-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="1929f-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="1929f-112">A parancsmagokkal kapcsolatos további információkért lásd az Azure Key Vault parancsmagokat ( a Microsoft Developer Network-tárban vagy a https://msdn.microsoft.com/library/azure/dn868052.aspx) Set-AzKeyVaultSecret parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="1929f-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="1929f-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1929f-113">EXAMPLES</span></span>

### <span data-ttu-id="1929f-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="1929f-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="1929f-115">Ez a vessző hozzáad egy tanúsítványt a keyvault és a megadott titkos azonosítóból.</span><span class="sxs-lookup"><span data-stu-id="1929f-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="1929f-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="1929f-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="1929f-117">Ez a vessző hozzáad egy tanúsítványkulcsot a megadott keyvault és titkos azonosítóból, pipázással.</span><span class="sxs-lookup"><span data-stu-id="1929f-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="1929f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1929f-118">PARAMETERS</span></span>

### <span data-ttu-id="1929f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1929f-119">-AsJob</span></span>
<span data-ttu-id="1929f-120">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="1929f-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1929f-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="1929f-121">-CertificateStore</span></span>
<span data-ttu-id="1929f-122">Azt a tanúsítványtárat adja meg a virtuális gépen, amelyhez a tanúsítványt hozzá kell adni.</span><span class="sxs-lookup"><span data-stu-id="1929f-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="1929f-123">A megadott tanúsítványtár implicit módon a LocalMachine-fiókban található.</span><span class="sxs-lookup"><span data-stu-id="1929f-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="1929f-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="1929f-124">-CertificateUrl</span></span>
<span data-ttu-id="1929f-125">Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="1929f-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="1929f-126">Ha titkos kulcsot szeretne hozzáadni a kulcstárhoz, tekintse meg a Kulcs vagy titkos kulcs \[ hozzáadása a kulcstárhoz ( \] . https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add)</span><span class="sxs-lookup"><span data-stu-id="1929f-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="1929f-127">Ebben az esetben a tanúsítványnak a Következő JSON-objektum Base64 kódolásúnak kell lennie, amely UTF-8 kódolású: \<br\> \<br\> { \<br\> "adatok":" \<Base64-encoded-certificate\> ", \<br\> "dataType":"pfx";"password":" \<br\> " \<pfx-file-password\> \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="1929f-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="1929f-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1929f-128">-ClusterName</span></span>
<span data-ttu-id="1929f-129">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="1929f-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1929f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1929f-130">-DefaultProfile</span></span>
<span data-ttu-id="1929f-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1929f-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1929f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1929f-132">-InputObject</span></span>
<span data-ttu-id="1929f-133">Node Type resource</span><span class="sxs-lookup"><span data-stu-id="1929f-133">Node Type resource</span></span>

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

### <span data-ttu-id="1929f-134">-Name</span><span class="sxs-lookup"><span data-stu-id="1929f-134">-Name</span></span>
<span data-ttu-id="1929f-135">Adja meg a csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="1929f-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="1929f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1929f-136">-ResourceGroupName</span></span>
<span data-ttu-id="1929f-137">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="1929f-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1929f-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1929f-138">-SourceVaultId</span></span>
<span data-ttu-id="1929f-139">A tanúsítványokat tartalmazó kulcstár erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="1929f-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="1929f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1929f-140">-Confirm</span></span>
<span data-ttu-id="1929f-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1929f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1929f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1929f-142">-WhatIf</span></span>
<span data-ttu-id="1929f-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1929f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1929f-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1929f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1929f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1929f-145">CommonParameters</span></span>
<span data-ttu-id="1929f-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1929f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1929f-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1929f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1929f-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1929f-148">INPUTS</span></span>

### <span data-ttu-id="1929f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1929f-149">System.String</span></span>

## <span data-ttu-id="1929f-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1929f-150">OUTPUTS</span></span>

### <span data-ttu-id="1929f-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1929f-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="1929f-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1929f-152">NOTES</span></span>

## <span data-ttu-id="1929f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1929f-153">RELATED LINKS</span></span>
