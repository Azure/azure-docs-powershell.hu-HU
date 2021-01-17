---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340002"
---
# <span data-ttu-id="91a49-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="91a49-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="91a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91a49-102">SYNOPSIS</span></span>
<span data-ttu-id="91a49-103">Biztonsági profil hozzáadása fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="91a49-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="91a49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91a49-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91a49-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91a49-105">DESCRIPTION</span></span>
<span data-ttu-id="91a49-106">A biztonsági profil egy biztonságos fürt egalizálásával való létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="91a49-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="91a49-107">A biztonsági profil a fürt Active Directory-tartományhoz való csatlakozásával kapcsolatos konfigurációkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="91a49-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="91a49-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91a49-108">EXAMPLES</span></span>

### <span data-ttu-id="91a49-109">1. példa: Biztonsági profil hozzáadása a fürtkonfigurációs objektumhoz</span><span class="sxs-lookup"><span data-stu-id="91a49-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="91a49-110">Ez a parancs hozzáad egy biztonsági profilértéket a -hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="91a49-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="91a49-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91a49-111">PARAMETERS</span></span>

### <span data-ttu-id="91a49-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="91a49-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="91a49-113">Az Ambari és Az ősök szolgáltatásban elérhető Active Directory-csoportok megkülönböztető nevei</span><span class="sxs-lookup"><span data-stu-id="91a49-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a49-114">-Config</span><span class="sxs-lookup"><span data-stu-id="91a49-114">-Config</span></span>
<span data-ttu-id="91a49-115">Ez a parancsmag által módosított HDInsight-fürtkonfigurációs objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a49-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="91a49-116">Ezt az objektumot a New-AzHDInsightClusterConfig hozta létre.</span><span class="sxs-lookup"><span data-stu-id="91a49-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91a49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a49-117">-DefaultProfile</span></span>
<span data-ttu-id="91a49-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="91a49-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91a49-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="91a49-119">-DomainResourceId</span></span>
<span data-ttu-id="91a49-120">A fürt Active Directory-tartományerőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="91a49-120">Active Directory domain resource id for the cluster.</span></span>

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

### <span data-ttu-id="91a49-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="91a49-121">-DomainUserCredential</span></span>
<span data-ttu-id="91a49-122">A tartományi felhasználói fiók hitelesítő adatai, amelyek megfelelő engedélyekkel rendelkeznek a fürt létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="91a49-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="91a49-123">A felhasználónévnek formátumban kell user@domain lennie</span><span class="sxs-lookup"><span data-stu-id="91a49-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a49-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="91a49-124">-LdapsUrls</span></span>
<span data-ttu-id="91a49-125">Egy vagy több LDAPS-kiszolgáló URL-címei az Active Directoryhoz</span><span class="sxs-lookup"><span data-stu-id="91a49-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a49-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="91a49-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="91a49-127">Annak az Active Directory-címtárnak a szervezeti egységének megkülönböztető neve, amelyben felhasználói és számítógépes fiókok fognak létrejönni</span><span class="sxs-lookup"><span data-stu-id="91a49-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a49-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91a49-128">-Confirm</span></span>
<span data-ttu-id="91a49-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="91a49-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91a49-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a49-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a49-131">CommonParameters</span></span>
<span data-ttu-id="91a49-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a49-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a49-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91a49-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a49-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91a49-134">INPUTS</span></span>

### <span data-ttu-id="91a49-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="91a49-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="91a49-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91a49-136">OUTPUTS</span></span>

### <span data-ttu-id="91a49-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="91a49-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="91a49-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91a49-138">NOTES</span></span>

## <span data-ttu-id="91a49-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91a49-139">RELATED LINKS</span></span>
