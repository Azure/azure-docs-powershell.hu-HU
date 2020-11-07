---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: 1f841d8cb49463f1ca9ce9198fc6173bb7efe506
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847593"
---
# <span data-ttu-id="f66c7-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="f66c7-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="f66c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f66c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f66c7-103">Biztonsági profilt ad hozzá a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f66c7-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="f66c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f66c7-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f66c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f66c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f66c7-106">A biztonsági profil segítségével biztonságos fürtöt hozhat létre a kerberizing.</span><span class="sxs-lookup"><span data-stu-id="f66c7-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="f66c7-107">A biztonsági profil a fürt Active Directory-tartományhoz való csatlakozásának konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f66c7-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="f66c7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f66c7-108">EXAMPLES</span></span>

### <span data-ttu-id="f66c7-109">1. példa: biztonsági profil hozzáadása a cluster Configuration objektumhoz</span><span class="sxs-lookup"><span data-stu-id="f66c7-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="f66c7-110">Ez a parancs a biztonsági profil értékét hozzáadja a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="f66c7-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f66c7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f66c7-111">PARAMETERS</span></span>

### <span data-ttu-id="f66c7-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="f66c7-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="f66c7-113">A Ambari és a Rangerben elérhető Active Directory-csoportok megkülönböztető nevei</span><span class="sxs-lookup"><span data-stu-id="f66c7-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="f66c7-114">-Config</span><span class="sxs-lookup"><span data-stu-id="f66c7-114">-Config</span></span>
<span data-ttu-id="f66c7-115">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f66c7-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f66c7-116">Ezt az objektumot az New-AzHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f66c7-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f66c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66c7-117">-DefaultProfile</span></span>
<span data-ttu-id="f66c7-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f66c7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f66c7-119">-Tartomány</span><span class="sxs-lookup"><span data-stu-id="f66c7-119">-Domain</span></span>
<span data-ttu-id="f66c7-120">A fürt Active Directory-tartománya</span><span class="sxs-lookup"><span data-stu-id="f66c7-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="f66c7-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="f66c7-121">-DomainUserCredential</span></span>
<span data-ttu-id="f66c7-122">A tartomány felhasználói fiókjának hitelesítő adatai, megfelelő engedélyekkel a fürt létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="f66c7-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="f66c7-123">A Felhasználónév user@domain formátuma</span><span class="sxs-lookup"><span data-stu-id="f66c7-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="f66c7-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="f66c7-124">-LdapsUrls</span></span>
<span data-ttu-id="f66c7-125">Az Active Directory egy vagy több LDAP-kiszolgálójának URL-címei</span><span class="sxs-lookup"><span data-stu-id="f66c7-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="f66c7-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="f66c7-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="f66c7-127">A szervezeti egység megkülönböztetett neve az Active Directoryban, ahol a felhasználói és a számítógépfiókok létrejönnek</span><span class="sxs-lookup"><span data-stu-id="f66c7-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="f66c7-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f66c7-128">-Confirm</span></span>
<span data-ttu-id="f66c7-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f66c7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f66c7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f66c7-130">-WhatIf</span></span>
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

### <span data-ttu-id="f66c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66c7-131">CommonParameters</span></span>
<span data-ttu-id="f66c7-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f66c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66c7-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f66c7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66c7-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f66c7-134">INPUTS</span></span>

### <span data-ttu-id="f66c7-135">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f66c7-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="f66c7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f66c7-136">OUTPUTS</span></span>

### <span data-ttu-id="f66c7-137">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="f66c7-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="f66c7-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f66c7-138">NOTES</span></span>

## <span data-ttu-id="f66c7-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f66c7-139">RELATED LINKS</span></span>